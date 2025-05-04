<script>
	import { onMount, afterUpdate } from 'svelte';
	import { browser } from '$app/environment';

	// Properti yang diterima komponen
	export let animation = 'fade';
	export let duration = 1;
	export let delay = 0;
	export let offset = 100; // Jarak tambahan dari bawah viewport (px)
	export let once = true;
	export let ease = 'power2.out';

	let element;

	async function initAnimation() {
		if (!browser || !element) return;

		try {
			const { gsap, ScrollTrigger } = await import('gsap/all');
			console.log('GSAP:', gsap, 'ScrollTrigger:', ScrollTrigger);
			console.log('Target element:', element);
			gsap.registerPlugin(ScrollTrigger);

			let fromProps = {};
			let toProps = { duration, delay, ease };

			switch (animation) {
				case 'fade':
					fromProps = { opacity: 0 };
					toProps.opacity = 1;
					break;
				case 'slide-up':
					fromProps = { y: 50, opacity: 0 };
					toProps.y = 0;
					toProps.opacity = 1;
					break;
				case 'slide-down':
					fromProps = { y: -50, opacity: 0 };
					toProps.y = 0;
					toProps.opacity = 1;
					break;
				case 'slide-left':
					fromProps = { x: 50, opacity: 0 };
					toProps.x = 0;
					toProps.opacity = 1;
					break;
				case 'slide-right':
					fromProps = { x: -50, opacity: 0 };
					toProps.x = 0;
					toProps.opacity = 1;
					break;
				case 'zoom-in':
					fromProps = { scale: 0.8, opacity: 0 };
					toProps.scale = 1;
					toProps.opacity = 1;
					break;
				default:
					fromProps = { opacity: 0 };
					toProps.opacity = 1;
			}

			const tween = gsap.fromTo(element, fromProps, {
				...toProps,
				scrollTrigger: {
					trigger: element,
					start: `top bottom-${offset}px`, // Mulai saat bagian atas elemen offset px dari bawah viewport
					end: `center center`, // Selesai saat tengah elemen mencapai tengah viewport
					toggleActions: once ? 'play none none none' : 'play none none reset',
					markers: true // Debugging
				}
			});

			return () => {
				tween.kill();
				ScrollTrigger.getById(element)?.kill();
			};
		} catch (error) {
			console.error('Error in AOS:', error);
		}
	}

	onMount(initAnimation);
	afterUpdate(initAnimation);
</script>

<div bind:this={element} class="contents">
	<slot />
</div>

<script>
	import welcome from '$lib/images/svelte-welcome.webp';
	import welcomeFallback from '$lib/images/svelte-welcome.png';
	import ProductPage from '$components/sections/ProductPage.svelte';
	import Hero from '$components/sections/Hero.svelte';
	import Feature from '$components/sections/Feature.svelte';
	import Faq from '$components/sections/Faq.svelte';

	const faqItems = [
		{
			title: 'Apa itu Svelte?',
			content:
				'Svelte adalah framework front-end modern yang mengkompilasi kode Anda menjadi JavaScript vanilla yang sangat efisien.'
		},
		{
			title: 'Bagaimana cara menginstall Svelte?',
			content:
				"Anda bisa menginstall Svelte dengan menjalankan perintah 'npx degit sveltejs/template nama-projek' kemudian 'cd nama-projek' dan 'npm install'."
		},
		{
			title: 'Apa keunggulan Svelte?',
			content:
				'Svelte tidak menggunakan virtual DOM seperti React atau Vue, melainkan mengkompilasi kode Anda menjadi update DOM yang sangat efisien saat build time.'
		}
	];
</script>

<svelte:head>
	<title>Home</title>
	<meta name="description" content="Svelte demo app" />
</svelte:head>

<Hero />
<Feature />
<ProductPage />
<Faq items={faqItems} multiple={true} />

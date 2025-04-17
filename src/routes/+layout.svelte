<script>
	import Header from '$components/sections/Header.svelte';
	import Footer from '$components/sections/Footer.svelte';
	import '../app.css';

	let { children } = $props();
</script>

<div class="app">
	<Header />

	<main>
		{@render children()}
	</main>

	<Footer />
</div>

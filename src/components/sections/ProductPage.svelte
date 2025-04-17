<script>
	import ProductCard from '$components/ProductCard.svelte';
	import CategoryFilter from '$components/CategoryFilter.svelte';
	import products from '$lib/data/product';

	const categories = [...new Set(products.map((product) => product.category))];

	let activeCategory = 'all';

	const handleFilter = (event) => {
		activeCategory = event.detail.category;
	};

	$: filteredProducts =
		activeCategory === 'all'
			? products
			: products.filter((product) => product.category === activeCategory);
</script>

<div
	class="relative border-t border-gray-200 bg-white px-8 py-10 md:py-16 lg:py-24 xl:px-0 xl:py-40"
>
	<div id="pricing" class="container mx-auto flex h-full max-w-6xl flex-col items-center">
		<h2 class="my-5 text-base font-medium tracking-tight text-indigo-500 uppercase">
			Silahkan klik tombol dibawah ini untuk melihat contoh
		</h2>
		<h3
			class="mt-2 w-full max-w-2xl px-5 text-center text-2xl leading-tight font-black text-gray-900 sm:mt-0 sm:px-0 sm:text-6xl md:px-0"
		>
			Pilihan Tema
		</h3>

		<div class="mx-auto max-w-full sm:px-8 md:max-w-6xl">
			<div class="container mx-auto px-4 py-8">
				<CategoryFilter {categories} {activeCategory} on:filter={handleFilter} />

				<div class="grid grid-cols-1 gap-6 sm:grid-cols-2 lg:grid-cols-3 xl:grid-cols-4">
					{#each filteredProducts as product}
						<ProductCard {product} />
					{/each}
				</div>

				{#if filteredProducts.length === 0}
					<div class="py-12 text-center">
						<p class="text-lg text-gray-500">No products found in this category.</p>
					</div>
				{/if}
			</div>
		</div>
	</div>
</div>

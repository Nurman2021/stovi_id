<script>
	let { product } = $props();
</script>

<div
	class="max-w-sm overflow-hidden rounded bg-white shadow-lg transition-shadow duration-300 hover:shadow-xl"
>
	<img class="h-48 w-full object-cover" src={product.image} alt={product.name} />
	<div class="px-6 py-4">
		<div class="mb-2 text-xl font-bold text-gray-800">{product.name}</div>
		<p class="mb-4 text-base text-gray-600">{product.description}</p>
		<div class="flex items-center justify-between">
			<span class="text-lg font-bold text-indigo-600">${product.price}</span>
			<button
				class="rounded bg-indigo-600 px-4 py-2 font-bold text-white transition-colors duration-300 hover:bg-indigo-700"
			>
				Add to Cart
			</button>
		</div>
	</div>
	<div class="px-6 pt-4 pb-2">
		{#each product.tags as tag}
			<span
				class="mr-2 mb-2 inline-block rounded-full bg-gray-200 px-3 py-1 text-sm font-semibold text-gray-700"
			>
				#{tag}
			</span>
		{/each}
	</div>
</div>

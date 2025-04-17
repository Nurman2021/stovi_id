<script>
	export let categories = [];
	export let activeCategory = 'all';

	const handleClick = (category) => {
		activeCategory = category;
		dispatch('filter', { category });
	};

	import { createEventDispatcher } from 'svelte';
	const dispatch = createEventDispatcher();
</script>

<div class="mb-8 flex flex-wrap justify-center gap-2">
	<button
		class={`rounded-full px-4 py-2 font-medium ${activeCategory === 'all' ? 'bg-indigo-600 text-white' : 'bg-gray-200 text-gray-700 hover:bg-gray-300'}`}
		on:click={() => handleClick('all')}
	>
		All Products
	</button>

	{#each categories as category}
		<button
			class={`rounded-full px-4 py-2 font-medium ${activeCategory === category ? 'bg-indigo-600 text-white' : 'bg-gray-200 text-gray-700 hover:bg-gray-300'}`}
			on:click={() => handleClick(category)}
		>
			{category}
		</button>
	{/each}
</div>

<script>
	import { ShoppingCart } from 'lucide-svelte';
</script>

<!-- Header Section -->
<header class="relative z-50 h-24 w-full">
	<div
		class="container mx-auto flex h-full max-w-6xl items-center justify-center px-8 sm:justify-between xl:px-0"
	>
		<a href="/" class="relative flex h-full items-center leading-none font-black">
			<svg
				class="h-6 w-auto fill-current text-indigo-600"
				viewBox="0 0 194 116"
				xmlns="http://www.w3.org/2000/svg"
			>
				<g fill-rule="evenodd">
					<path
						d="M96.869 0L30 116h104l-9.88-17.134H59.64l47.109-81.736zM0 116h19.831L77 17.135 67.088 0z"
					/>
					<path d="M87 68.732l9.926 17.143 29.893-51.59L174.15 116H194L126.817 0z" />
				</g>
			</svg>
			<span class="ml-3 text-xl text-gray-800">OurWedding<span class="text-pink-500">.</span></span>
		</a>

		<div
			class="absolute left-0 mt-48 hidden w-full flex-col items-center justify-center border-b border-gray-200 pb-8 md:relative md:mt-0 md:flex md:w-auto md:flex-row md:items-end md:justify-between md:border-none md:bg-transparent md:p-0"
		>
			<a
				href="#feature"
				class="fold-bold relative z-40 flex h-full w-full items-center gap-2 rounded bg-indigo-700 px-5 py-2 text-sm font-bold text-white shadow-md transition-all duration-300 hover:shadow-xl sm:w-full lg:bg-white lg:text-indigo-700 lg:shadow-none"
			>
				<ShoppingCart />
				Pesan
			</a>
			<!-- class="absolute top-0 right-1/2 -z-10 -mt-64 -ml-12 hidden w-screen min-w-6xl opacity-50 lg:block" -->

			<img src="/img/floral-1.png" alt="header ilustration" class="" />
		</div>
	</div>
</header>
<!-- End Header Section-->

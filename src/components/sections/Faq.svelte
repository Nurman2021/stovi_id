<script>
	import Whatsapp from '$components/icons/Whatsapp.svelte';
	import { ThumbsUpIcon, MessageSquareLockIcon } from 'lucide-svelte';

	export let items = [];
	export let multiple = false;
	let activeIndices = [];

	import { ChevronDown } from 'lucide-svelte';

	function toggleItem(index) {
		if (multiple) {
			// Mode multiple: toggle item tertentu
			activeIndices = activeIndices.includes(index)
				? activeIndices.filter((i) => i !== index)
				: [...activeIndices, index];
		} else {
			// Mode single: hanya satu item yang bisa terbuka
			activeIndices = activeIndices[0] === index ? [] : [index];
		}
	}

	function toggleAll(open) {
		if (open) {
			activeIndices = items.map((_, index) => index);
		} else {
			activeIndices = [];
		}
	}
</script>

<div class=" border-t border-gray-200 px-8 py-10 md:py-16 lg:py-24 xl:px-0 xl:py-40">
	<section class="mx-auto flex max-w-6xl flex-col items-center">
		<h2 class="my-5 text-base font-medium tracking-tight text-indigo-500 uppercase">
			Cara order undangan digital
		</h2>
		<h3
			class="mt-2 w-full max-w-3xl px-5 text-center text-2xl leading-tight font-black text-gray-900 sm:mt-0 sm:px-0 sm:text-6xl md:px-0"
		>
			FAQ
		</h3>
		<div class="mt-2 w-full max-w-3xl overflow-hidden rounded-lg border border-gray-200">
			<!-- {#if multiple}
				<div class="flex space-x-2 bg-gray-50 p-2">
					<button
						on:click={() => toggleAll(true)}
						class="rounded bg-blue-500 px-3 py-1 text-xs text-white transition hover:bg-blue-600"
					>
						Buka Semua
					</button>
					<button
						on:click={() => toggleAll(false)}
						class="rounded bg-gray-500 px-3 py-1 text-xs text-white transition hover:bg-gray-600"
					>
						Tutup Semua
					</button>
				</div>
			{/if} -->

			{#each items as item, index}
				<div class="border-b border-gray-200 last:border-b-0">
					<button
						on:click={() => toggleItem(index)}
						class="flex w-full items-center justify-between p-4 text-left transition hover:bg-gray-50
						 {activeIndices.includes(index) ? 'bg-gray-50 font-medium' : ''}"
						aria-expanded={activeIndices.includes(index)}
						aria-controls={`accordion-panel-${index}`}
					>
						<span>{item.title}</span>
						<span
							class="transform text-gray-500 transition-transform duration-200
							  {activeIndices.includes(index) ? 'rotate-180' : ''}"
						>
							<ChevronDown strokeWidth={1} />
						</span>
					</button>

					<div
						id={`accordion-panel-${index}`}
						class="overflow-hidden transition-all duration-200
						 {activeIndices.includes(index) ? 'max-h-96 p-4' : 'max-h-0'}"
						role="region"
					>
						<div class="pb-2">
							{@html item.content}
						</div>
					</div>
				</div>
			{/each}
		</div>

		<h2 class="my-5 text-base font-medium tracking-tight text-indigo-500 uppercase">
			Add-Ons Layanan
		</h2>
		<p class="max-w-3xl text-center font-semibold text-black/70 italic">
			Kami menawarkan layanan tambahan lain yang bisa menjadikan momen bahagia anda menjadi lebih
			mudah & berkesan. Semua "disiapkan spesial untuk Anda".
		</p>

		<div class="mt-4 flex w-full max-w-3xl flex-col gap-3">
			<div class="flex w-full items-center gap-1">
				<strong class=" w-60">Custom Warna & Font</strong>
				<div class="w-full border-b-2 border-dotted border-black"></div>
				<p>Rp.45rb</p>
			</div>
			<p class=" text-sm">Perubahan desain untuk tampilan warna dan huruf pendukung</p>
			<div class="flex w-full items-center gap-1">
				<strong class=" w-36">Request Tema</strong>
				<div class="w-full border-b-2 border-dotted border-black"></div>
				<p>Rp.199rb</p>
			</div>
			<p class="text-sm">Bantu kamu buat undangan sesuai keinginan</p>
		</div>

		<div class="mt-10 grid w-full max-w-2xl grid-cols-2 grid-rows-2 gap-4">
			<div
				class="flex items-center justify-center gap-2 text-2xl font-bold tracking-wider text-indigo-500/50"
			>
				<ThumbsUpIcon size={48} />JAMINAN <br /> KEPUASAN
			</div>
			<div
				class="flex items-center justify-center gap-2 text-2xl font-bold tracking-wider text-indigo-500/50"
			>
				<MessageSquareLockIcon size={48} /> TRANSAKSI <br /> AMAN
			</div>
			<div
				class="col-span-2 row-start-2 flex w-full transform cursor-pointer items-center justify-center gap-2 rounded-lg px-5 py-3 tracking-wider text-pink-500 shadow-md transition duration-400 hover:-translate-y-1 hover:bg-pink-500 hover:text-white hover:shadow-xl"
			>
				<Whatsapp />
				HUBUNGI KAMI VIA WHATSAPP
			</div>
		</div>
	</section>
</div>

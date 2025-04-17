<script>
	import { Award, Music, Sparkles, Users, RefreshCw, Zap } from 'lucide-svelte';
</script>

<!-- BEGIN FEATURES SECTION -->
<div
	id="features"
	class="relative w-full border-t border-gray-200 px-8 py-10 md:py-16 lg:py-24 xl:px-0 xl:py-40"
>
	<div class="container mx-auto flex h-full max-w-6xl flex-col items-center justify-between">
		<h2 class="my-5 text-base font-medium tracking-tight text-indigo-500 uppercase">
			Fitur Menarik Yang Akan Membuat Undangan Tampil Beda.
		</h2>
		<h3
			class="mt-2 max-w-2xl px-5 text-center text-3xl leading-tight font-black text-gray-900 sm:mt-0 sm:px-0 sm:text-6xl"
		>
			Fitur Terlengkap
		</h3>
		<div class="mt-0 flex w-full flex-col sm:mt-10 lg:mt-20 lg:flex-row">
			<div class="mx-auto mb-0 w-full max-w-md p-4 sm:mb-16 lg:mb-0 lg:w-1/3">
				<div
					class="relative mr-5 flex h-full w-full flex-col items-center justify-center rounded-lg p-20"
				>
					<svg
						class="absolute h-full w-full fill-current text-gray-100"
						viewBox="0 0 377 340"
						xmlns="http://www.w3.org/2000/svg"
					>
						<g>
							<g>
								<path
									d="M342.8 3.7c24.7 14 18.1 75 22.1 124s18.6 85.8 8.7 114.2c-9.9 28.4-44.4 48.3-76.4 62.4-32 14.1-61.6 22.4-95.9 28.9-34.3 6.5-73.3 11.1-95.5-6.2-22.2-17.2-27.6-56.5-47.2-96C38.9 191.4 5 151.5.9 108.2-3.1 64.8 22.7 18 61.8 8.7c39.2-9.2 91.7 19 146 16.6 54.2-2.4 110.3-35.6 135-21.6z"
								/>
							</g>
						</g>
					</svg>
					<!-- FEATURE Icon 1 -->
					<div
						class="z-10 flex h-20 w-20 items-center justify-center rounded-3xl bg-gradient-to-br from-cyan-400 to-blue-800 text-white"
					>
						<Zap size={40} strokeWidth={1} />
					</div>
					<h4 class="relative mt-6 text-lg font-bold">Pengerjaan Cepat</h4>
					<p class="relative mt-2 text-center text-base text-gray-600">
						Proses cepat kurang dari 24 jam!
					</p>
				</div>
			</div>

			<div class="mx-auto mb-0 w-full max-w-md p-4 sm:mb-16 lg:mb-0 lg:w-1/3">
				<div
					class="relative mr-5 flex h-full w-full flex-col items-center justify-center rounded-lg p-20"
				>
					<svg
						class="absolute h-full w-full fill-current text-gray-100"
						viewBox="0 0 358 372"
						xmlns="http://www.w3.org/2000/svg"
					>
						<g>
							<g>
								<path
									d="M315.7 6.5c30.2 15.1 42.6 61.8 41.5 102.5-1.1 40.6-15.7 75.2-24.3 114.8-8.7 39.7-11.3 84.3-34.3 107.2-23 22.9-66.3 23.9-114.5 30.7-48.2 6.7-101.3 19.1-123.2-4.1-21.8-23.2-12.5-82.1-21.6-130.2C30.2 179.3 2.6 141.9.7 102c-2-39.9 21.7-82.2 57.4-95.6 35.7-13.5 83.3 2.1 131.2 1.7 47.9-.4 96.1-16.8 126.4-1.6z"
								/>
							</g>
						</g>
					</svg>
					<!-- FEATURE Icon 2 -->
					<div
						class="z-10 flex h-20 w-20 items-center justify-center rounded-3xl bg-gradient-to-br from-cyan-400 to-blue-800 text-white"
					>
						<RefreshCw size={40} strokeWidth={1} />
					</div>
					<h4 class="relative mt-6 text-lg font-bold">Revisi Tak Terbatas</h4>
					<p class="relative mt-2 text-center text-base text-gray-600">
						Bebas request revisi sampai hari-H. Puas? Kami baru berhenti!
					</p>
				</div>
			</div>

			<div class="mx-auto mb-16 w-full max-w-md p-4 lg:mb-0 lg:w-1/3">
				<div
					class="relative mr-5 flex h-full w-full flex-col items-center justify-center rounded-lg p-20"
				>
					<svg
						class="absolute h-full w-full fill-current text-gray-100"
						viewBox="0 0 378 410"
						xmlns="http://www.w3.org/2000/svg"
					>
						<g>
							<g>
								<path
									d="M305.9 14.4c23.8 24.6 16.3 84.9 26.6 135.1 10.4 50.2 38.6 90.3 43.7 137.8 5.1 47.5-12.8 102.4-50.7 117.4-37.9 15.1-95.7-9.8-151.7-12.2-56.1-2.5-110.3 17.6-130-3.4-19.7-20.9-4.7-82.9-11.5-131.2C25.5 209.5-3 174.7 1.2 147c4.2-27.7 41-48.3 75-69.6C110.1 56.1 141 34.1 184 17.5c43.1-16.6 98.1-27.7 121.9-3.1z"
								/>
							</g>
						</g>
					</svg>
					<!-- FEATURE Icon 3 -->
					<div
						class="z-10 flex h-20 w-20 items-center justify-center rounded-3xl bg-gradient-to-br from-cyan-400 to-blue-800 text-white"
					>
						<Users size={40} strokeWidth={1} />
					</div>
					<h4 class="relative mt-6 text-lg font-bold">Tamu Unlimited</h4>
					<p class="relative mt-2 text-center text-base text-gray-600">
						Undang sebanyak mungkin tamu tanpa khawatir biaya tambahan. Semua bisa hadir!
					</p>
				</div>
			</div>
		</div>
	</div>

	<div class="container mx-auto flex h-full max-w-6xl flex-col items-center justify-between">
		<div class="mt-0 flex w-full flex-col sm:mt-10 lg:mt-20 lg:flex-row">
			<div class="mx-auto mb-0 w-full max-w-md p-4 sm:mb-16 lg:mb-0 lg:w-1/3">
				<div
					class="relative mr-5 flex h-full w-full flex-col items-center justify-center rounded-lg p-20"
				>
					<svg
						class="absolute h-full w-full fill-current text-gray-100"
						viewBox="0 0 377 340"
						xmlns="http://www.w3.org/2000/svg"
					>
						<g>
							<g>
								<path
									d="M342.8 3.7c24.7 14 18.1 75 22.1 124s18.6 85.8 8.7 114.2c-9.9 28.4-44.4 48.3-76.4 62.4-32 14.1-61.6 22.4-95.9 28.9-34.3 6.5-73.3 11.1-95.5-6.2-22.2-17.2-27.6-56.5-47.2-96C38.9 191.4 5 151.5.9 108.2-3.1 64.8 22.7 18 61.8 8.7c39.2-9.2 91.7 19 146 16.6 54.2-2.4 110.3-35.6 135-21.6z"
								/>
							</g>
						</g>
					</svg>
					<!-- FEATURE Icon 1 -->
					<div
						class="z-10 flex h-20 w-20 items-center justify-center rounded-3xl bg-gradient-to-br from-cyan-400 to-blue-800 text-white"
					>
						<Music size={40} strokeWidth={1} />
					</div>
					<h4 class="relative mt-6 text-lg font-bold">Request Musik Bebas</h4>
					<p class="relative mt-2 text-center text-base text-gray-600">
						Mau lagu apa saja? Kami siapkan playlist khusus sesuai permintaan Anda.
					</p>
				</div>
			</div>

			<div class="mx-auto mb-0 w-full max-w-md p-4 sm:mb-16 lg:mb-0 lg:w-1/3">
				<div
					class="relative mr-5 flex h-full w-full flex-col items-center justify-center rounded-lg p-20"
				>
					<svg
						class="absolute h-full w-full fill-current text-gray-100"
						viewBox="0 0 358 372"
						xmlns="http://www.w3.org/2000/svg"
					>
						<g>
							<g>
								<path
									d="M315.7 6.5c30.2 15.1 42.6 61.8 41.5 102.5-1.1 40.6-15.7 75.2-24.3 114.8-8.7 39.7-11.3 84.3-34.3 107.2-23 22.9-66.3 23.9-114.5 30.7-48.2 6.7-101.3 19.1-123.2-4.1-21.8-23.2-12.5-82.1-21.6-130.2C30.2 179.3 2.6 141.9.7 102c-2-39.9 21.7-82.2 57.4-95.6 35.7-13.5 83.3 2.1 131.2 1.7 47.9-.4 96.1-16.8 126.4-1.6z"
								/>
							</g>
						</g>
					</svg>
					<!-- FEATURE Icon 2 -->
					<div
						class="z-10 flex h-20 w-20 items-center justify-center rounded-3xl bg-gradient-to-br from-cyan-400 to-blue-800 text-white"
					>
						<Sparkles size={40} strokeWidth={1} />
					</div>
					<h4 class="relative mt-6 text-lg font-bold">Desain Eksklusif</h4>
					<p class="relative mt-2 text-center text-base text-gray-600">
						Konsep premium dengan sentuhan profesional. Visual mewah yang bikin acara makin
						berkesan!
					</p>
				</div>
			</div>

			<div class="mx-auto mb-16 w-full max-w-md p-4 lg:mb-0 lg:w-1/3">
				<div
					class="relative mr-5 flex h-full w-full flex-col items-center justify-center rounded-lg p-20"
				>
					<svg
						class="absolute h-full w-full fill-current text-gray-100"
						viewBox="0 0 378 410"
						xmlns="http://www.w3.org/2000/svg"
					>
						<g>
							<g>
								<path
									d="M305.9 14.4c23.8 24.6 16.3 84.9 26.6 135.1 10.4 50.2 38.6 90.3 43.7 137.8 5.1 47.5-12.8 102.4-50.7 117.4-37.9 15.1-95.7-9.8-151.7-12.2-56.1-2.5-110.3 17.6-130-3.4-19.7-20.9-4.7-82.9-11.5-131.2C25.5 209.5-3 174.7 1.2 147c4.2-27.7 41-48.3 75-69.6C110.1 56.1 141 34.1 184 17.5c43.1-16.6 98.1-27.7 121.9-3.1z"
								/>
							</g>
						</g>
					</svg>
					<!-- FEATURE Icon 3 -->
					<div
						class="z-10 flex h-20 w-20 items-center justify-center rounded-3xl bg-gradient-to-br from-cyan-400 to-blue-800 text-white"
					>
						<Award size={40} strokeWidth={1} />
					</div>
					<h4 class="relative mt-6 text-lg font-bold">Kualitas Terbaik</h4>
					<p class="relative mt-2 text-center text-base text-gray-600">
						Standar tinggi di setiap detail. Hasil memukau yang bikin semua orang terpesona
					</p>
				</div>
			</div>
		</div>
	</div>
</div>
<!-- END FEATURES SECTION -->

<script>
	import welcome from '$lib/images/svelte-welcome.webp';
	import welcomeFallback from '$lib/images/svelte-welcome.png';
	import ProductPage from '$components/sections/ProductPage.svelte';
	import Hero from '$components/sections/Hero.svelte';
	import Feature from '$components/sections/Feature.svelte';
	import Faq from '$components/sections/Faq.svelte';

	const faqItems = [
		{
			title: 'Pesan Undangan Digital',
			content: `
        <ol class="list-decimal pl-5 space-y-2">
          <li>Pilih Tema undangan yang diinginkan. Untuk melihat demo, silahkan klik bagian katalog</li>
          <li>Untuk melihat halaman tampilan demo, silahkan klik tombol “Lihat Demo”, dan catat nomor demo yang diinginkan.</li>
          <li>Setelah memilih tema undangan, Anda bisa melakukan pemesanan dengan melakukan pemesanan dengan langsung melakukan klik pada tombol order.</li>
          <li>Isi format yang disediakan, dan lakukan pembayaran sesuai dengan pilihan metode pembayaran yang ada.</li>
        </ol>
      `
		},
		{
			title: 'Proses Pengerjaan Orderan',
			content: `
        <ul class="list-disc pl-5 space-y-2">
          <li>Silahkan lakukan pembayaran dengan jenis paket yang dipilih setelah undangan selesai dikerjakan dengan cara transfer via bank ke akun bank kami berikan.</li>
          <li>Jaminan Proses pengerjaan <strong> Max 24 Jam </strong> dari masa order</li>
        </ul>
      `
		},
		{
			title: 'Daftar Sumber Belajar',
			content: `
        <p class="pl-5 space-y-2">
         Jika mengalami kesulitan dalam pemesanan jasa undangan digital kami, silahkan kontak kami melalui chat support whatsapp di: 0857-5121-2616
        </p>
        <p class="mt-4 pl-5"><strong>Kami akan dengan senang hati siap membantu Anda.</strong></p>
      `
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

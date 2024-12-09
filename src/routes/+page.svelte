<script>
// @ts-nocheck

	import { Gallery } from 'flowbite-svelte';
	const images1 = [
		{ alt: 'erbology', src: 'https://flowbite.s3.amazonaws.com/docs/gallery/masonry/image.jpg' },
		{ alt: 'shoes', src: 'https://flowbite.s3.amazonaws.com/docs/gallery/masonry/image-1.jpg' },
		{ alt: 'small bag', src: 'https://flowbite.s3.amazonaws.com/docs/gallery/masonry/image-2.jpg' }
	];
	const images2 = [
		{ alt: 'plants', src: 'https://flowbite.s3.amazonaws.com/docs/gallery/masonry/image-3.jpg' },
		{ alt: 'watch', src: 'https://flowbite.s3.amazonaws.com/docs/gallery/masonry/image-4.jpg' },
		{ alt: 'shoe', src: 'https://flowbite.s3.amazonaws.com/docs/gallery/masonry/image-5.jpg' }
	];
	const images3 = [
		{ alt: 'cream', src: 'https://flowbite.s3.amazonaws.com/docs/gallery/masonry/image-6.jpg' },
		{ alt: 'small bag', src: 'https://flowbite.s3.amazonaws.com/docs/gallery/masonry/image-7.jpg' },
		{ alt: 'lamp', src: 'https://flowbite.s3.amazonaws.com/docs/gallery/masonry/image-8.jpg' }
	];
	const images4 = [
		{ alt: 'toiletbag', src: 'https://flowbite.s3.amazonaws.com/docs/gallery/masonry/image-9.jpg' },
		{ alt: 'playstation', src: 'https://flowbite.s3.amazonaws.com/docs/gallery/masonry/image-10.jpg' },
		{ alt: 'bag', src: 'https://flowbite.s3.amazonaws.com/docs/gallery/masonry/image-11.jpg' }
	];
</script>

<header class="w-full px-4 py-4">
	<div class="w-full bg-pink-400 text-white flex justify-center items-center h-48 rounded-lg">
		<h1 class="p-4 text-7xl font-bold font-sans uppercase">Nosa Gallery</h1>
	</div>
</header>

<section class="w-full flex flex-col gap-4 pt-10 pb-20 px-4">
	<Gallery class="gap-4 grid-cols-2">
		<img src="https://flowbite.s3.amazonaws.com/docs/gallery/square/image-1.jpg" alt="shoas" class="h-auto max-w- rounded-lg" />
		<div class="h-auto max-w- rounded-lg flex items-center justify-center text-2xl sm:text-6xl font-extrabold bg-red-300">
			Smart
		</div>
		<div class="h-auto max-w- rounded-lg flex items-center justify-center text-2xl sm:text-6xl font-extrabold bg-blue-300">
			Creative
		</div>
		<img alt="plants" src="https://flowbite.s3.amazonaws.com/docs/gallery/square/image-3.jpg" class="h-auto max-w- rounded-lg" />
	</Gallery>
	<Gallery class="gap-4 grid-cols-2 md:grid-cols-4">
		<Gallery items={images1} />
		<Gallery items={images2} />
		<Gallery items={images3} />
		<Gallery items={images4} />
	</Gallery>
</section>

<footer class="w-full px-4 py-4">
	<div class="w-full bg-pink-400 text-white flex justify-center items-center h-10 rounded-lg">
		<h1 class="p-4 text-sm font-bold font-sans uppercase">Nosa Gallery</h1>
	</div>
</footer>
<script>
// @ts-nocheck
	import { Gallery } from 'flowbite-svelte';

	const images = [
		{ type: 'text', text: 'Aspire', bgColor: 'bg-pink-400', color: ''},
		{ type: 'img', alt: 'painting', src: '/img/1.jpeg' },
		{ type: 'text', text: 'Innovate', bgColor: 'bg-blue-400', color: ''},
		{ type: 'img', alt: 'painting', src: '/img/2.jpeg' },
		{ type: 'text', text: 'Design', bgColor: 'bg-pink-400', color: ''},
		{ type: 'img', alt: 'painting', src: '/img/3.jpeg' },
		{ type: 'img', alt: 'painting', src: '/img/4.jpeg' },
		{ type: 'text', text: 'Thrive', bgColor: 'bg-pink-400', color: ''},
		{ type: 'img', alt: 'painting', src: '/img/5.jpeg' },
		{ type: 'img', alt: 'painting', src: '/img/6.jpeg' },
		{ type: 'img', alt: 'painting', src: '/img/7.jpeg' },
		{ type: 'text', text: 'Achieve', bgColor: 'bg-blue-400', color: ''},
		{ type: 'img', alt: 'painting', src: '/img/8.jpeg' },
		{ type: 'img', alt: 'painting', src: '/img/9.jpeg' },
		{ type: 'text', text: 'Motivate', bgColor: 'bg-pink-400', color: ''},
		{ type: 'img', alt: 'painting', src: '/img/10.jpeg'},
		{ type: 'text', text: 'Create', bgColor: 'bg-blue-400', color: ''},
	]
</script>

<header class="w-full flex flex-col">
	<div class="w-full flex flex-col gap-1 bg-pink-400 text-white justify-center items-center pt-20">
		<h1 class="p-4 text-6xl md:text-8xl font-bold font-sans uppercase">Nosa Gallery</h1>
		<h3 class="p-4 text-2xl font-bold font-sans uppercase underline underline-offset-8 italic">
			Welcome to the Infinite Canvas of Imagination
		</h3>
	</div>
	<div class="w-full h-full">
		<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1440 320"><path fill="#f17eb8" fill-opacity="1" d="M0,288L60,272C120,256,240,224,360,213.3C480,203,600,213,720,213.3C840,213,960,203,1080,170.7C1200,139,1320,85,1380,58.7L1440,32L1440,0L1380,0C1320,0,1200,0,1080,0C960,0,840,0,720,0C600,0,480,0,360,0C240,0,120,0,60,0L0,0Z"></path></svg>
	</div>
</header>

<section class="w-full flex items-center justify-center">
	<div class="w-full lg:w-2/3 flex flex-col justify-center items-center gap-8 px-4">
		<Gallery class="gap-2 grid-cols-2">
			<img src="/img/1.jpeg" alt="creative" class="h-auto max-w- rounded-lg" />
			<div class="h-auto max-w- rounded-lg flex items-center justify-center text-2xl sm:text-4xl md:text-5xl lg:text-6xl font-extrabold bg-pink-400 uppercase">
				Inspiration
			</div>
			<div class="h-auto max-w- rounded-lg flex items-center justify-center text-2xl sm:text-4xl md:text-5xl lg:text-6xl font-extrabold bg-blue-400 uppercase">
				Creativity
			</div>
			<img alt="smart" src="/img/2.jpeg" class="h-auto max-w- rounded-lg" />
		</Gallery>
	
		<div class="w-full md:w-1/2 flex flex-col bg-white gap-20 p-12 my-20 rounded-2xl border-4 border-x-0 border-t-blue-400 border-b-pink-400 text-center">
			<p class="text-white text-xs md:text-base flex items-center justify-center">
				<span class=" bg-pink-400 rounded-md rounded-r-none font-bold py-1 px-2 md:py-2 md:px-4 uppercase">imagine</span>
				<span class=" bg-blue-400 font-bold py-1 px-2 md:py-2 md:px-4 uppercase">create</span>
				<span class=" bg-pink-400 rounded-r-none font-bold py-1 px-2 md:py-2 md:px-4 uppercase">enjoy</span>
				<span class=" bg-blue-400 rounded-r-none font-bold py-1 px-2 md:py-2 md:px-4 uppercase">inspire</span>
				<span class=" bg-pink-400 rounded-md rounded-l-none font-bold py-1 px-2 md:py-2 md:px-4 uppercase">repeat</span>
			</p>
		</div>

		<div class="masonry sm:masonry-sm md:masonry-md">
			{#each images as img, index}
				<div class="break-inside py-1">
					{#if img.type == 'text'}
						<div
							class="flex-1 h-40 md:h-96 max-w- rounded-lg flex items-center justify-center text-2xl lg:text-6xl font-extrabold uppercase {img.bgColor || 'bg-pink-400'} {img.color || 'text-gray-900'} ">
							{img.text}
						</div>
					{:else}
						<img src="{img.src}" alt="{img.alt}" class="flex-1 h-full w-full inset-0 rounded-lg bg-gray-50 object-cover" />
					{/if}
				</div>
			{/each}
		</div>
	</div>
</section>

<footer class="w-full text-center">
	<div class="w-full h-full">
		<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1440 320"><path fill="#f17eb8" fill-opacity="1" d="M0,288L60,272C120,256,240,224,360,213.3C480,203,600,213,720,213.3C840,213,960,203,1080,170.7C1200,139,1320,85,1380,58.7L1440,32L1440,320L1380,320C1320,320,1200,320,1080,320C960,320,840,320,720,320C600,320,480,320,360,320C240,320,120,320,60,320L0,320Z"></path></svg>
	</div>
	<h1 class="p-4 m-0 text-lg font-bold font-sans uppercase bg-pink-400 text-white underline underline-offset-8 italic">
		Nosa Gallery
	</h1>
</footer>
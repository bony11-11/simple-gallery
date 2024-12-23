<script>
	import Card from '$lib/card.svelte';

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

<section class="w-full flex items-center justify-center">
	<div class="w-full lg:w-2/3 flex flex-col justify-center items-center gap-8 px-4 text-white">
		<div class="grid gap-4 grid-cols-2">
			<Card src="/img/1.jpeg" alt="inspiration"/>
			<div class="h-auto max-w- rounded-lg flex items-center justify-center text-2xl sm:text-4xl md:text-5xl lg:text-6xl font-extrabold bg-pink-400 uppercase">
				Inspiration
			</div>
			<div class="h-auto max-w- rounded-lg flex items-center justify-center text-2xl sm:text-4xl md:text-5xl lg:text-6xl font-extrabold bg-blue-400 uppercase">
				Creativity
			</div>
			<Card src="/img/2.jpeg" alt="Creativity"/>
		</div>
	
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
							class="flex-1 h-40 md:h-96 max-w- rounded-lg flex items-center justify-center text-2xl lg:text-6xl font-extrabold uppercase {img.bgColor || 'bg-pink-400'} {img.color || 'text-white'} ">
							{img.text}
						</div>
					{:else}
						<Card src="{img.src}" alt="{img.alt}"/>
					{/if}
				</div>
			{/each}
		</div>
	</div>
</section>

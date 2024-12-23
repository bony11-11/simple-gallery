<script lang="ts">
	import '../app.css';
</script>

<header class="w-full flex flex-col">
	<div class="w-full flex flex-col gap-1 bg-pink-400 text-white justify-center items-center pt-20 text-center">
		<h1 class="p-4 text-6xl md:text-8xl font-bold font-sans uppercase">The Artist's Mind <br /> Gallery</h1>
		<h3 class="p-4 text-2xl font-bold font-sans uppercase underline underline-offset-8 italic">
			This is our special place for art<br /> Anything is possible here!
		</h3>
	</div>
	<div class="w-full h-full">
		<svg xmlns="http://www.w3.org/2000/svg" class=" opacity-100" viewBox="0 0 1440 320"><path fill="#f472b6" fill-opacity="1" d="M0,288L60,272C120,256,240,224,360,213.3C480,203,600,213,720,213.3C840,213,960,203,1080,170.7C1200,139,1320,85,1380,58.7L1440,32L1440,0L1380,0C1320,0,1200,0,1080,0C960,0,840,0,720,0C600,0,480,0,360,0C240,0,120,0,60,0L0,0Z"></path></svg>
	</div>
</header>

<slot />

<footer class="w-full text-center p-0 m-0">
	<div class="w-full h-full inset-0">
		<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1440 320"><path fill="#f472b6" fill-opacity="1" d="M0,288L60,272C120,256,240,224,360,213.3C480,203,600,213,720,213.3C840,213,960,203,1080,170.7C1200,139,1320,85,1380,58.7L1440,32L1440,320L1380,320C1320,320,1200,320,1080,320C960,320,840,320,720,320C600,320,480,320,360,320C240,320,120,320,60,320L0,320Z"></path></svg>
	</div>
	<h1 class="p-8 m-0 text-sm sm:text-lg font-bold font-sans uppercase bg-pink-400 text-white underline underline-offset-8 italic">
		Brought to you by Leen the Artist
	</h1>
</footer>

<script>
	// @ts-ignore
	import { fly, fade } from 'svelte/transition';
	import Hero from '../components/sections/Hero.svelte';
	import About from '../components/sections/About.svelte';
	import AboutCode from '../components/sections/AboutCode.svelte';
	import Skills from '../components/sections/Skills.svelte';
	import Resume from '../components/sections/Resume.svelte';
	import Projects from '../components/sections/Projects.svelte';
	import BackToTop from '../components/BackToTop.svelte';
</script>

<svelte:head>
	<title>James Montebell</title>
</svelte:head>

<div class="hero">
	<Hero />
</div>

<div class="flex flex-col text-xl">
	<div class="md:flex md:flex-row-reverse md:w-full md:px-20 p-6 md:py-10 md:justify-center">
		<div id="About" />
		<div class="md:self-center">
			<AboutCode />
		</div>
		<About />
	</div>
	<div id="Resume" />
	<!-- <hr class="bg-[#202330] w-3/4 self-center my-6 border-2 rounded-full" /> -->
	<Skills />
	<!-- <hr class="bg-[#202330] w-3/4 self-center my-6 border-2 rounded-full" /> -->
	<div class="md:w-2/3 md:self-center">
		<Resume />
	</div>
	<!-- <hr class="bg-[#202330] w-3/4 self-center my-6 border-2 rounded-full" /> -->
	<div id="Projects" class="mt-6">
		<Projects />
	</div>
</div>
<div class="sticky bottom-10 left-[80%]">
	<!-- <a class="font-medium text-left text-xl md:mt-6 bg-[#d4163c] w-full h-screen" href="/">JM</a> -->
	<BackToTop />
</div>

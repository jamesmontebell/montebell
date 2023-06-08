<script lang="ts">
	import { fly } from 'svelte/transition';
	import AnimatedHamburger from './../components/AnimatedHamburger.svelte';
	import '../app.postcss';
	import Menu from '../components/Menu.svelte';
	import Icon from '@iconify/svelte';

	let open: boolean;
	function openOutlook() {
		window.open('mailto:jmontebell2@gulls.salisbury.edu', '_blank');
	}
	function openLinkedin() {
		window.open('https://www.linkedin.com/in/james-montebell-223456233/', '_blank');
	}

	function openGithub() {
		window.open('https://github.com/jamesmontebell', '_blank');
	}
</script>

<div>
	<div class="relative z-10">
		<div class="flex justify-between fixed top-0 w-full bg-[#2b2e40] shadow-md">
			<div class="md:hidden justify-center m-4 ml-6 flex bg-[#d4163c] p-2 rounded-full">
				<a class="font-medium text-left text-sm text-[#dfe0e2] md:mt-6 bg-transparent" href="/"
					>JM</a
				>
			</div>
			<div class="md:flex justify-center ml-12 m-4 hidden">
				<a
					class="font-medium text-left hover:scale-110 transition hover:ease-in-out hover:duration-500 text-[#dfe0e2]"
					href="/">Hi, I'm James.</a
				>
			</div>
			<!-- DESKTOP VIEW -->
			<div class="hidden md:flex">
				<div class="justify-center items-center mr-12 gap-6 flex font-regular">
					<p
						transition:fly={{ y: -15, delay: 50 * 1 }}
						class="hover:scale-110 transition hover:ease-in-out duration-200"
					>
						<button
							class="hover:scale-110 transition hover:ease-in-out hover:duration-500 text-[#dfe0e2]"
							on:click={() => {
								open = false;
								const element = document.getElementById('About');

								const y = element.getBoundingClientRect().top + window.pageYOffset - 100;

								window.scrollTo({ top: y, behavior: 'smooth' });
							}}>About</button
						>
					</p>
					<p
						transition:fly={{ y: -15, delay: 50 * 1 }}
						class="hover:scale-110 transition hover:ease-in-out duration-200"
					>
						<button
							class="hover:scale-110 transition hover:ease-in-out hover:duration-500 text-[#dfe0e2]"
							on:click={() => {
								open = false;
								const element = document.getElementById('Resume');

								const y = element.getBoundingClientRect().top + window.pageYOffset - 100;

								window.scrollTo({ top: y, behavior: 'smooth' });
							}}>Resume</button
						>
					</p>
					<p
						transition:fly={{ y: -15, delay: 50 * 1 }}
						class="hover:scale-110 transition hover:ease-in-out duration-200"
					>
						<button
							class="hover:scale-110 transition hover:ease-in-out hover:duration-500 text-[#dfe0e2]"
							on:click={() => {
								open = false;
								const element = document.getElementById('Projects');

								const y = element.getBoundingClientRect().top + window.pageYOffset - 100;

								window.scrollTo({ top: y, behavior: 'smooth' });
							}}>Projects</button
						>
					</p>
					<a
						class=" hover:scale-110 transition hover:ease-in-out hover:duration-500 text-[#dfe0e2]"
						href="/contact">Contact</a
					>
				</div>
			</div>
			<nav class="flex justify-end mr-4 md:hidden">
				<AnimatedHamburger bind:open />
			</nav>
		</div>
		<div class="fixed w-full top-14 md:hidden">
			<Menu bind:open />
		</div>
	</div>

	<div class="text-[#dfe0e2]">
		<slot />
	</div>

	<div class="flex flex-col items-center p-4 gap-4 text-[#dfe0e2]">
		<div class="text-2xl font-bold text-center">James Montebell</div>
		<div class="flex gap-4 justify-center">
			<button on:click={openOutlook}>
				<Icon class="text-3xl transition-all hover:scale-125" icon="file-icons:microsoft-outlook" />
			</button>
			<button on:click={openGithub}>
				<Icon class="text-4xl transition-all hover:scale-125" icon="mdi:github" />
			</button>
			<button on:click={openLinkedin}>
				<Icon class="text-4xl  transition-all hover:scale-125" icon="mdi:linkedin" />
			</button>
		</div>
		<div class="text-sm">Made with ❤️ in Delaware.</div>
	</div>
	<!-- <div class="sticky bottom-10 left-[80%] rounded-full w-fit h-fit bg-[#d4163c] p-2">
		<a class="font-medium text-left text-xl md:mt-6 bg-[#d4163c] w-full h-screen" href="/">JM</a>
	</div> -->
</div>

<style>
	/* @import url('https://fonts.googleapis.com/css2?family=Montserrat:ital,wght@0,100;0,200;0,300;0,400;0,500;0,600;0,700;0,800;0,900;1,100;1,200;1,300;1,400;1,500;1,600;1,700;1,800;1,900&display=swap'); */
	@import url('https://fonts.googleapis.com/css2?family=Sora:wght@100;200;300;400;500;600;700;800&display=swap');
	* {
		/* font-family: 'Montserrat', sans-serif; */
		font-family: 'Sora', sans-serif;
	}
</style>

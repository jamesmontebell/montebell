<script>
	import { Avatar, AvatarFallback, AvatarImage } from '$components/ui/avatar';
	import Icon from '@iconify/svelte';
	import { fly, fade } from 'svelte/transition';

	import { onMount } from 'svelte';

	function openOutlook() {
		window.open('mailto:jmontebell2@gulls.salisbury.edu', '_blank');
	}
	function openLinkedin() {
		window.open('https://www.linkedin.com/in/james-montebell-223456233/', '_blank');
	}

	function openGithub() {
		window.open('https://github.com/jamesmontebell', '_blank');
	}

	let code = `James Montebell: {
        Age: 23,
        Major: Computer Science,
        Location: Lewes, DE,
        Graduation: Dec 2023
    }`;
	let language = 'javascript';

	onMount(() => window.scrollTo(0, 0));
</script>

<div
	class="flex flex-col items-center gap-2
	
	md:flex-row-reverse md:justify-evenly"
	id="top"
	in:fly={{ y: -15, delay: 50 * 15 }}
	out:fade
>
	<Avatar
		class="w-60 h-60 mt-[95px] shadow-2xl
	
	md:mt-36 md:w-72 md:h-72 md:shadow-2xl
	"
	>
		<AvatarImage class="" src="src/lib/images/me.jpg" alt="@shadcn" />
		<AvatarFallback>CN</AvatarFallback>
	</Avatar>
	<div class="mt-10 md:mt-36">
		<div class="self-start ml-4">Hello, I'm...</div>
		<div
			class="self-start text-3xl font-bold text-left ml-4
		
					md:text-7xl
		"
		>
			James <br /> Montebell
		</div>
		<div
			class="self-start m-4 font-light
		
					md:text-sm

		"
		>
			Undergraduate Student @ Salisbuy University
		</div>
		<div class="flex mt-4 gap-4 justify-center">
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
	</div>
</div>
<svg
	width="100%"
	height="100%"
	id="svg"
	viewBox="0 0 1440 490"
	xmlns="http://www.w3.org/2000/svg"
	class="transition duration-300 ease-in-out delay-150"
	><path
		d="M 0,500 C 0,500 0,166 0,166 C 137.2,172.13333333333333 274.4,178.26666666666668 427,189 C 579.6,199.73333333333332 747.5999999999999,215.06666666666663 919,212 C 1090.4,208.93333333333337 1265.2,187.4666666666667 1440,166 C 1440,166 1440,500 1440,500 Z"
		stroke="none"
		stroke-width="0"
		fill="#27293a"
		fill-opacity="0.53"
		class="transition-all duration-300 ease-in-out delay-150 path-0"
	/><path
		d="M 0,500 C 0,500 0,333 0,333 C 101.86666666666667,352.3333333333333 203.73333333333335,371.66666666666663 391,357 C 578.2666666666667,342.33333333333337 850.9333333333334,293.6666666666667 1040,284 C 1229.0666666666666,274.3333333333333 1334.5333333333333,303.66666666666663 1440,333 C 1440,333 1440,500 1440,500 Z"
		stroke="none"
		stroke-width="0"
		fill="#27293a"
		fill-opacity="1"
		class="transition-all duration-300 ease-in-out delay-150 path-1"
	/></svg
>

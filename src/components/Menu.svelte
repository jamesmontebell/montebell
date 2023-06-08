<script lang="ts">
	import { fly, scale, slide } from 'svelte/transition';
	import { quadOut } from 'svelte/easing';

	export let open: boolean;
</script>

{#if open}
	<div transition:slide class="h-screen flex flex-col justify-center text-[#dfe0e2]">
		{#each ['About', 'Resume', 'Projects', 'Contact'] as link, i}
			{#if link == 'About'}
				<p
					transition:fly={{ y: -15, delay: 50 * i }}
					class="hover:scale-110 transition hover:ease-in-out duration-200"
				>
					<button
						class="font-black uppercase text-3xl md:text-5xl no-underline text-[#dfe0e2]"
						on:click={() => {
							open = false;
							const element = document.getElementById('About');
							const y = element.getBoundingClientRect().top + window.pageYOffset - 100;

							window.scrollTo({ top: y, behavior: 'smooth' });
						}}>About</button
					>
				</p>
			{:else if link == 'Resume'}
				<p
					transition:fly={{ y: -15, delay: 50 * i }}
					class="hover:scale-110 transition hover:ease-in-out duration-200"
				>
					<button
						class="font-black uppercase text-3xl md:text-5xl no-underline text-[#dfe0e2]"
						on:click={() => {
							open = false;
							const element = document.getElementById('Resume');
							const y = element.getBoundingClientRect().top + window.pageYOffset - 100;

							window.scrollTo({ top: y, behavior: 'smooth' });
						}}>Resume</button
					>
				</p>
			{:else if link == 'Projects'}
				<p
					transition:fly={{ y: -15, delay: 50 * i }}
					class="hover:scale-110 transition hover:ease-in-out duration-200"
				>
					<button
						class="font-black uppercase text-3xl md:text-5xl no-underline text-[#dfe0e2]"
						on:click={() => {
							open = false;
							const element = document.getElementById('Projects');
							const y = element.getBoundingClientRect().top + window.pageYOffset - 100;

							window.scrollTo({ top: y, behavior: 'smooth' });
						}}>Projects</button
					>
				</p>
			{:else if link == 'Contact'}
				<p
					transition:fly={{ y: -15, delay: 50 * i }}
					class="hover:scale-110 transition hover:ease-in-out duration-200"
				>
					<a
						href="/contact"
						class="font-black uppercase text-3xl md:text-5xl no-underline"
						on:click={() => {
							open = false;
						}}>Contact</a
					>
				</p>
			{:else}
				<p transition:fly={{ y: -15, delay: 50 * i }}>
					{link}
				</p>
			{/if}
		{/each}
	</div>

	<!-- <hr  transition:scale={{ duration: 750, easing: quadOut, opacity: 1 }} /> -->
{/if}

<style>
	div {
		text-align: center;
		font-size: 1.5em;
		letter-spacing: 0.15em;
		padding: 1em;
		padding-top: 0;
		color: 'black';
		position: absolute;
		background-color: #2b2e40;
		width: 100%;
	}
	p {
		cursor: pointer;
		width: max-content;
		margin: 1rem auto;
	}
</style>

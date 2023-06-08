<script>
	export let showOnPx = 150;
	let hidden = true;

	function goTop() {
		document.body.scrollIntoView({ behavior: 'smooth' });
	}

	function scrollContainer() {
		return document.documentElement || document.body;
	}

	function handleOnScroll() {
		if (!scrollContainer()) {
			return;
		}

		if (scrollContainer().scrollTop > showOnPx) {
			hidden = false;
		} else {
			hidden = true;
		}
	}
	import Icon from '@iconify/svelte';
</script>

<svelte:window on:scroll={handleOnScroll} />

<!-- svelte-ignore a11y-click-events-have-key-events -->
<div
	class="back-to-top rounded-full w-fit h-fit bg-[#d4163c] p-2 cursor-pointer"
	on:click={goTop}
	class:hidden
>
	<Icon icon="clarity:arrow-line" class="bg-transparent" />
</div>

<style>
	.back-to-top {
		opacity: 1;
		transition: opacity 1s, visibility 0.5s;
		position: fixed;
		z-index: 99;
		right: 20px;
		user-select: none;
		bottom: 20px;
		color: white;
	}

	.back-to-top.hidden {
		opacity: 0;
		visibility: hidden;
		transition: all;
	}
</style>

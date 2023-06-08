<script lang="ts">
	import {
		Card,
		CardContent,
		CardDescription,
		CardFooter,
		CardHeader,
		CardTitle
	} from '$components/ui/card';

	export let img: string;
	export let title: string;
	export let desc: string;
	export let view: string;
	export let wip: boolean;
</script>

<Card class="flex flex-col md:w-60 justify-between text-[#dfe0e2]">
	<CardHeader>
		<img class="w-40 h-20 object-cover rounded-lg self-center" src={img} alt="Bruh" />
		<CardTitle class="text-2xl font-bold">{title}</CardTitle>
	</CardHeader>
	<CardContent>
		<p class="text-base bg-[#202330]">{desc}</p>
	</CardContent>
	<CardFooter class="flex justify-between">
		<button
			class="peer p-2 bg-[#d4163c] rounded-xl transition-all transform hover:scale-110 ease-in-out"
		>
			<a class="bg-transparent" href={view}>View</a>
		</button>
		{#if wip}
			<button
				class="peer text-xs p-2 bg-[#e4c25e] text-black rounded-xl transition-all transform hover:scale-110 ease-in-out"
			>
				<a class="bg-transparent" href={view}>Work in progress</a>
			</button>
		{/if}
	</CardFooter>
</Card>

<script>
	import Project from '../Project.svelte';
</script>

<div class="p-4 flex flex-wrap gap-6">
	<Project
		img="src/components/flikshop.png"
		title="Flikshop LMS"
		desc="Flikshop is a Learning Management System (LMS) made with Android Studio using Kotlin and XML."
		view="/"
		wip={false}
	/>
	<Project
		img="src/components/this.png"
		title="This Website"
		desc="This site was built using SvelteKit, TailwindCSS, TypeScript, Shadcn, and more."
		view="/"
		wip={false}
	/>
	<Project
		img="src/components/pokedexsvelte.png"
		title="SvelteKit Pokedex"
		desc="This site was built using SvelteKit, TailwindCSS, TypeScript, PokeAPI, and more."
		view="https://sveltekit-pokedex-taupe.vercel.app/"
		wip={false}
	/>
	<Project
		img="src/components/cz.png"
		title="CZCreative"
		desc="Built using SvelteKit, TailwindCSS, TypeScript, and more."
		view="/"
		wip={true}
	/>
	<Project
		img="src/components/pokedexjs.png"
		title="PokedexJS"
		desc="Built with HTML, CSS, JavaScript, and PokeAPI."
		view="https://jamesmontebell.github.io/PokeJsDex/"
		wip={false}
	/>
	<Project
		img="src/components/anime.png"
		title="ANIME-DB"
		desc="Built using SvelteKit, TailwindCSS, TypeScript, KitsuAPI, and more."
		view="/"
		wip={true}
	/>
</div>

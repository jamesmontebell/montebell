<script>
	import Prism from 'svelte-prism';

	let code = `James Montebell: {
        Age: 23,
        Major: Computer Science,
        Location: Lewes, DE,
        Graduation: Dec 2023
    }`;
	let language = 'javascript';
</script>

<link
	rel="stylesheet"
	href="https://cdnjs.cloudflare.com/ajax/libs/prism-themes/1.9.0/prism-one-dark.min.css"
/>
<div class="text-[14px] md:text-xs m-6 rounded-xl shadow-2xl border-2 border-[#d4163c] w-70">
	<div class="object-fill h-full w-full" />
	<Prism {language} source={code} />
</div>

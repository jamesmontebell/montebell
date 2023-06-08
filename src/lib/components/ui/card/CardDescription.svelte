<script lang="ts">
	import { cn } from '$lib/utils';

	let className: string | undefined | null = undefined;
	export { className as class };
</script>

<p class={cn('text-sm text-muted-foreground bg-[#202330]', className)} {...$$restProps}>
	<slot />
</p>

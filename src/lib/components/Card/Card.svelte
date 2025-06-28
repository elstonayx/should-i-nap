<script lang="ts">
	import type { Snippet } from 'svelte';

	let { className, children }: { className?: string; children: Snippet<[]> } = $props();
</script>

<div
	data-slot="card"
	class={[
		'rounded-base flex flex-col',
		'shadow-shadow border-border bg-background border-2',
		'text-foreground font-base gap-6',
		'py-6',
		className
	]}
>
	{@render children()}
</div>

<script lang="ts">
	import type { Snippet } from 'svelte';

	let { className, children }: { className?: string; children: Snippet<[]> } = $props();
</script>

<div
	data-slot="card-header"
	class={[
		'@container/card-header',
		'grid auto-rows-min grid-rows-[auto_auto]',
		'items-start gap-1.5 px-6',
		'has-[data-slot=card-action]:grid-cols-[1fr_auto]',
		'[.border-b]:pb-6',
		className
	]}
>
	{@render children()}
</div>

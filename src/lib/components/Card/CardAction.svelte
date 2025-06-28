<script lang="ts">
	import type { Snippet } from 'svelte';

	let { className, children }: { className?: string; children: Snippet<[]> } = $props();
</script>

<div
	data-slot="card-action"
	class={['col-start-2 row-span-2 row-start-1 self-start justify-self-end', className]}
>
	{@render children()}
</div>

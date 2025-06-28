<script lang="ts">
	import type { Snippet } from 'svelte';

	let { className, children }: { className?: string; children: Snippet<[]> } = $props();
</script>

<div data-slot="card-footer" class={['flex items-center px-6', '[.border-t]:pt-6', className]}>
	{@render children()}
</div>

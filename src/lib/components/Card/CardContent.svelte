<script lang="ts">
	import type { Snippet } from 'svelte';

	let { className, children }: { className?: string; children: Snippet<[]> } = $props();
</script>

<div data-slot="card-content" class={['px-6', className]}>
	{@render children()}
</div>

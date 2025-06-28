<script lang="ts">
	import type { Snippet } from 'svelte';

	let { className, children }: { className?: string; children: Snippet<[]> } = $props();
</script>

<div data-slot="card-title" class={['font-heading leading-none', className]}>
	{@render children()}
</div>

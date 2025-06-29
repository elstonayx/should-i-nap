<script lang="ts">
	import type { Snippet } from 'svelte';

	type Props = {
		src: string;
		alt: string;
		caption?: string;
		className?: string;
	};
	let { src, alt, caption, className }: Props = $props();
</script>

<figure
	class={[
		'rounded-base border-border bg-main font-base shadow-shadow w-[250px] overflow-hidden border-2',
		className
	]}
>
	<img class="w-full" {src} {alt} />
	{#if caption}
		<figcaption class={['border-border text-main-foreground border-t-2 p-4']}>
			{caption}
		</figcaption>
	{/if}
</figure>

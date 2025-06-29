<script lang="ts">
	import '../app.css';

	let { children } = $props();
</script>

<div
	class={[
		'grid h-screen grid-cols-[1fr_auto_1fr] grid-rows-[1fr_auto_1fr]',
		'[&>*]:col-start-2 [&>*]:row-start-2'
	]}
>
	{@render children()}
</div>

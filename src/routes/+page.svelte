<script>
	import Card from '$lib/components/Card/Card.svelte';
	import CardHeader from '$lib/components/Card/CardHeader.svelte';
	import CardTitle from '$lib/components/Card/CardTitle.svelte';
	import CardContent from '$lib/components/Card/CardContent.svelte';
	import CardFooter from '$lib/components/Card/CardFooter.svelte';
	import CardAction from '$lib/components/Card/CardAction.svelte';
	import Button from '$lib/components/Button/Button.svelte';
</script>

<svelte:head>
	<title>Should I nap? 💤</title>
	<link rel="icon" href="https://fav.farm/💤" />
	<meta name="description" content="Should I nap? 💤" />
	<meta name="viewport" content="width=device-width, initial-scale=1.0" />
	<meta name="apple-mobile-web-app-capable" content="yes" />
	<meta name="apple-mobile-web-app-status-bar-style" content="black" />
	<meta name="apple-mobile-web-app-title" content="Should I nap? 💤" />
</svelte:head>

<div
	class={[
		'grid h-screen grid-cols-[1fr_auto_1fr] grid-rows-[1fr_auto_1fr]',
		'[&>*]:col-start-2 [&>*]:row-start-2'
	]}
>
	<Card className="bg-secondary-background w-[500px]">
		<CardHeader>
			<CardTitle className="text-4xl font-bold">Should I nap? 💤</CardTitle>
		</CardHeader>
		<CardContent>
			<div class="flex flex-col gap-3">
				<p class="font-normal">
					Feeling sleepy?<br />
					You could power through and be a legend…<br />
					or take a nap and dream about being productive.
				</p>
				<p class="font-normal">
					Let this highly unqualified app decide your fate.<br />Scientific? No.<br />
					Accurate? Also no.<br />
					Honest? Maybe. <br />
					🛏 Click the button. Embrace destiny.
				</p>
			</div>
		</CardContent>
		<CardFooter>
			<CardAction>
				<a href="https://www.youtube.com/watch?v=dQw4w9WgXcQ" target="_blank">
					<Button size="lg">Should I nap?</Button>
				</a>
			</CardAction>
		</CardFooter>
	</Card>
</div>

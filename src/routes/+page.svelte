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
</svelte:head>

<div
	class={[
		'grid h-screen grid-cols-[1fr_auto_1fr] grid-rows-[1fr_auto_1fr]',
		'[&>*]:col-start-2 [&>*]:row-start-2'
	]}
>
	<Card className="bg-secondary-background min-sm:w-[500px] w-80">
		<CardHeader>
			<CardTitle className="text-3xl min-sm:text-4xl font-bold">Should I nap? 💤</CardTitle>
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
			<CardAction className="w-full">
				<a href="/check">
					<Button size="lg" className="w-full">Should I nap?</Button>
				</a>
			</CardAction>
		</CardFooter>
	</Card>
</div>

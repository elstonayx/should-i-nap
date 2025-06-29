<script>
	import Card from '$lib/components/Card/Card.svelte';
	import CardContent from '$lib/components/Card/CardContent.svelte';
	import CardHeader from '$lib/components/Card/CardHeader.svelte';
	import CardTitle from '$lib/components/Card/CardTitle.svelte';
	import ImageCard from '$lib/components/ImageCard/ImageCard.svelte';
	import Button from '$lib/components/Button/Button.svelte';
	import CardFooter from '$lib/components/Card/CardFooter.svelte';
	import CardAction from '$lib/components/Card/CardAction.svelte';
</script>

<Card className="bg-secondary-background min-sm:w-[500px] w-80">
	<CardHeader>
		<CardTitle className="text-4xl font-bold">Should I nap? 💤</CardTitle>
	</CardHeader>
	<CardContent>
		<div class="flex justify-center">
			<ImageCard src="/images/cat-typing/1.gif" className="w-full" alt="cat typing" />
		</div>
	</CardContent>
	<CardFooter>
		<CardAction className="w-full">
			<Button size="lg" state="loading" className="w-full">Loading...</Button>
		</CardAction>
	</CardFooter>
</Card>

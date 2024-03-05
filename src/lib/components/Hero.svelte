<script>
	import HeroCarousel from '$lib/components/HeroCarousel.svelte';
	import { Button } from '$lib/components/ui/button';
</script>

<section class="flex items-center justify-center gap-8">
	<div class="flex flex-col items-center gap-5">
		<h2 class="text-center text-3xl font-bold tracking-tighter md:text-5xl">
			Your Old School RuneScape tasks, managed.
		</h2>
		<Button class="w-1/4" href="/tasks">Get started</Button>
	</div>
	<HeroCarousel />
</section>

<script lang="ts">
	import * as Card from '$lib/components/ui/card/index.js';
	import * as Carousel from '$lib/components/ui/carousel/index.js';
	import Autoplay from 'embla-carousel-autoplay';

	const plugin = Autoplay({ delay: 4000, stopOnInteraction: false });

	// The content for each card in the carousel
	const cardContent = [
		{
			title: 'Track your tasks easily',
			description: 'The best way to organize your osrs tasks.'
		},
		{
			title: 'Optimize your playtime',
			description: 'Set goals, and optimize your playtime.'
		},
		{
			title: 'Achieve your goals',
			description: 'Set goals and track your progress.'
		}
	];
</script>

<Carousel.Root plugins={[plugin]} class="w-full max-w-md">
	<Carousel.Content>
		{#each cardContent as { title, description }, i}
			<Carousel.Item>
				<Card.Root class="border-none">
					<Card.Content class="flex aspect-video flex-col items-center justify-center gap-3 p-6">
						<h2 class="font-bold tracking-tighter sm:text-4xl md:text-3xl/none">
							{title}
						</h2>
						<p class=" text-gray-500 md:text-lg">
							{description}
						</p>
					</Card.Content>
				</Card.Root>
			</Carousel.Item>
		{/each}
	</Carousel.Content>
	<Carousel.Previous />
	<Carousel.Next />
</Carousel.Root>

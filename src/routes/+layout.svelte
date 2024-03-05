<script>
	import '../app.pcss';
	import Header from '$lib/components/Header.svelte';
</script>

<main class="flex min-h-screen flex-col bg-muted">
	<section class="container mt-6">
		<Header />
		<slot />
	</section>
</main>

<script context="module" lang="ts">
	export const prerender = true;
</script>

<script lang="ts">
	import Counter from '$lib/Counter/index.svelte';

	const x: number = 123;
</script>

<svelte:head>
	<title>Home</title>
</svelte:head>

<section>
	<h1>Welcome to this site</h1>
	<h2>
		try editing <strong>src/routes/index.svelte</strong>
	</h2>

	{x}
	<Counter />
</section>

<style>
	section {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		flex: 1;
	}

	h1 {
		width: 100%;
	}
</style>

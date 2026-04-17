<script lang="ts">
	import '../app.css';
	import favicon from '$lib/assets/favicon.svg';

	let { children } = $props();
</script>

<svelte:head>
	<title>Myles Goodhue</title>
	<meta name="description" content="Internet software, built to last." />
	<meta property="og:title" content="Myles Goodhue" />
	<meta property="og:description" content="Internet software, built to last." />
	<link rel="icon" href={favicon} />
</svelte:head>

{@render children()}

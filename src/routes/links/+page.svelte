<script lang="ts">
	import LinkList from '$lib/components/LinkList.svelte';
</script>

<main class="min-h-screen max-w-5xl px-8 md:px-16 lg:px-24 pt-32 pb-24">
	<header class="mb-20">
		<h1 class="font-display text-[clamp(2.5rem,6vw,5rem)] leading-tight tracking-tight text-paper mb-4">
			Links
		</h1>
		<p class="font-sans text-base text-paper/50">
			Things I find useful, interesting, or worth returning to.
		</p>
	</header>

	<LinkList />

	<div class="mt-20 pt-8 border-t border-paper/10">
		<a
			href="/"
			class="back-link font-sans text-sm tracking-[0.15em] uppercase text-paper/40 hover:text-paper/70"
		>
			&larr; Back
		</a>
	</div>
</main>

<style>
	.back-link {
		transition: color 0.2s ease;
	}
</style>

<script lang="ts">
	import Hero from '$lib/components/Hero.svelte';
	import Expertise from '$lib/components/Expertise.svelte';
	import Contact from '$lib/components/Contact.svelte';
</script>

<main class="min-h-screen max-w-5xl">
	<Hero />
	<Expertise />
	<Contact />
	<footer class="px-8 md:px-16 lg:px-24 py-12 border-t border-paper/10">
		<a
			href="/links"
			class="footer-link font-sans text-sm tracking-[0.15em] uppercase text-paper/40 hover:text-paper/70"
		>
			Links &amp; resources &rarr;
		</a>
	</footer>
</main>

<style>
	.footer-link {
		transition: color 0.2s ease;
	}
</style>

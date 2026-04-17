<script lang="ts">
	let sectionEl: HTMLElement;
	let visible = $state(false);

	const specialties = [
		'ColdFusion', 'Python', 'Java', 'JavaScript',
		'REST & SOA', 'Oracle / MySQL / PostgreSQL', 'Microservices',
		'Architecture', 'Team Lead', 'UX & Documentation'
	];

	$effect(() => {
		const observer = new IntersectionObserver(
			([entry]) => {
				if (entry.isIntersecting) {
					visible = true;
					observer.disconnect();
				}
			},
			{ threshold: 0.2 }
		);
		observer.observe(sectionEl);
		return () => observer.disconnect();
	});
</script>

<section bind:this={sectionEl} class="px-8 md:px-16 lg:px-24 py-20 border-t border-paper/10">
	<p class="text-xs tracking-[0.2em] uppercase text-paper/30 font-sans mb-8">Specialties</p>
	<div class="flex flex-wrap gap-x-5 gap-y-3">
		{#each specialties as item, i}
			<span
				class="specialty text-sm md:text-base font-sans text-paper/60"
				class:visible
				style="transition-delay: {i * 45}ms"
			>
				{item}
			</span>
		{/each}
	</div>
</section>

<style>
	.specialty {
		opacity: 0;
		transform: translateY(10px);
		transition: opacity 0.5s ease, transform 0.5s ease;
	}
	.specialty.visible {
		opacity: 1;
		transform: translateY(0);
	}
</style>

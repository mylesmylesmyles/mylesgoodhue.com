<script lang="ts">
	import { fly } from 'svelte/transition';
	import { cubicOut } from 'svelte/easing';
</script>

<section class="px-8 md:px-16 lg:px-24 pt-32 pb-24">
	<div in:fly={{ y: 28, duration: 700, easing: cubicOut }}>
		<h1 class="font-display text-[clamp(3.5rem,10vw,8rem)] leading-[0.95] tracking-tight text-paper mb-8">
			Myles Goodhue
		</h1>
		<p class="text-xs tracking-[0.25em] uppercase text-amber mb-10 font-sans">
			Internet software, built to last.
		</p>
		<p class="font-sans text-base md:text-lg text-paper/70 max-w-[52ch] leading-relaxed">
			Twenty years designing and deploying internet-scale business software —
			from server infrastructure to software architecture to the interface
			people actually use. I plan, build, and ship highly available, secure
			systems. Top Secret/Secret NATO cleared.
		</p>
	</div>
</section>

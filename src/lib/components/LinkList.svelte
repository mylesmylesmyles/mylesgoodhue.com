<script lang="ts">
	import { links } from '$lib/data/links';

	const grouped = links.reduce<Record<string, typeof links>>((acc, link) => {
		(acc[link.category] ??= []).push(link);
		return acc;
	}, {});

	const categories = Object.keys(grouped).sort();
</script>

{#if categories.length === 0}
	<p class="font-sans text-paper/40 text-sm">No links added yet.</p>
{:else}
	<div class="flex flex-col gap-12">
		{#each categories as category}
			<div>
				<p class="text-xs tracking-[0.2em] uppercase text-paper/30 font-sans mb-5">{category}</p>
				<ul class="flex flex-col gap-4">
					{#each grouped[category] as link}
						<li>
							<a
								href={link.url}
								target="_blank"
								rel="noopener noreferrer"
								class="link-item font-sans text-base text-paper/80 hover:text-paper"
							>
								{link.title}
							</a>
							{#if link.note}
								<p class="text-sm text-paper/40 mt-1 font-sans">{link.note}</p>
							{/if}
						</li>
					{/each}
				</ul>
			</div>
		{/each}
	</div>
{/if}

<style>
	.link-item {
		position: relative;
		display: inline-block;
		transition: color 0.2s ease;
	}
	.link-item::after {
		content: '';
		position: absolute;
		bottom: -2px;
		left: 0;
		right: 0;
		height: 1px;
		background: currentColor;
		clip-path: inset(0 100% 0 0);
		transition: clip-path 0.35s ease;
	}
	.link-item:hover::after {
		clip-path: inset(0 0% 0 0);
	}
</style>

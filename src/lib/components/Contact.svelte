<section class="px-8 md:px-16 lg:px-24 py-20 border-t border-paper/10">
	<div class="md:ml-auto md:max-w-xs">
		<p class="text-xs tracking-[0.2em] uppercase text-paper/30 font-sans mb-8">Get in touch</p>
		<div class="flex flex-col gap-4">
			<a
				href="mailto:contact@mylesgoodhue.com"
				class="contact-link font-sans text-lg text-paper/80 hover:text-paper"
			>
				contact@mylesgoodhue.com
			</a>
			<a
				href="https://linkedin.com/in/mylesgoodhue"
				target="_blank"
				rel="noopener noreferrer"
				class="contact-link font-sans text-lg text-paper/80 hover:text-paper"
			>
				LinkedIn &rarr;
			</a>
		</div>
	</div>
</section>

<style>
	.contact-link {
		position: relative;
		display: inline-block;
		transition: color 0.2s ease;
	}
	.contact-link::after {
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
	.contact-link:hover::after {
		clip-path: inset(0 0% 0 0);
	}
</style>

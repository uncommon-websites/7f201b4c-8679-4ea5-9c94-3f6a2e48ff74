<!--
@component AboutTeaser
An engaging founder story teaser that builds personal connection and company credibility.
-->
<script lang="ts">
	// Types
	type Founder = {
		name: string;
		role: string;
		image: string;
		quote: string;
	};

	// Components
	import Button from "../ui/Button.svelte";
	import ScrollText from "./sub/ScrollText.svelte";

	// State
	let sectionRef: HTMLElement;

	let props = $props();

	// Data
	const founder: Founder = {
		name: "Kareem Arab",
		role: "Founder",
		image: "/generated/image-a-confident-tech-founder-poses-for-a-pro.webp",
		quote: "I built Wealth OS because I got tired of spending Sundays manually updating spreadsheets just to know where my money was. I needed something smarter—and cleaner—than anything on the market."
	};
</script>

<section bind:this={sectionRef} {...props}>
	<div class="section-px section-py container mx-auto">
		<div class="relative mx-auto grid max-w-2xl place-items-center gap-16">
			<ScrollText
				class="text-title1 text-center"
				text={`"${founder.quote}"`}
			/>

			<!-- Founder & CTA Section -->
			<div class="grid items-center gap-8 dark:border-gray-800">
				<div class="flex items-center justify-start gap-4">
					<img
						src={founder.image}
						alt={founder.name}
						class="size-12 rounded-full object-cover"
					/>
					<div>
						<div class="text-callout">{founder.name}</div>
						<div class="text-caption text-emphasis-low">{founder.role}</div>
					</div>
					<Button href="/about" variant="secondary" size="sm" class="ml-8">Our story</Button>
				</div>
			</div>
		</div>
	</div>
</section>

<script lang="ts">
	// Components
	import CallToAction from "$lib/components/layout/CallToAction.svelte";

	// Icons
	import StakeholderGrid from "$lib/components/layout/StakeholderGrid.svelte";
	import Story from "./Story.svelte";
	import SecondaryHero from "$lib/components/layout/hero-sections/SecondaryHero.svelte";
	import Culture from "$lib/components/layout/Culture.svelte";

	// Constants
	const values = [
		{
			title: "Clarity first",
			description: "We believe financial decisions should be made with complete information, not scattered data."
		},
		{
			title: "Privacy by design",
			description: "Your financial data belongs to you. We build security and privacy into every feature from day one."
		},
		{
			title: "Ruthless simplicity",
			description: "Complex financial systems shouldn't require complex interfaces. We distill complexity into clarity."
		}
	];
</script>

<SecondaryHero
	generating
	title="Solving world hunger"
	subtitle="one step at a time"
	imageSrc="https://www.unc.mn/image-placeholder.svg"
/>

<!-- Story Section -->
<Story
	generating
	paragraphs={[
		"We started in 2018 with a simple goal: make helpful tech that people actually need. While many chase profits, we chose to do things differently.",
		"Beyond making good products, we care about doing the right thing, being kind to our planet, and making sure everyone can use what we build. That's our compass.",
		"From day one, we've asked ourselves: 'Does this actually help people?' This question gets us through tough calls and shapes who we are. We're playing the long game here.",
		"We think about how our work affects real people's lives. We build tech that brings people together, keeps your information safe, and treats everyone fairly. When we stick to these basics, good things happen."
	]}
/>

<!-- Our Culture Section -->
<Culture {values} />

<!-- StakeholderGrid Section -->
<StakeholderGrid
	stakeholderType="team"
	title="Meet the founder."
	subtitle="Building financial clarity for the modern professional."
	stakeholders={[
		{
			name: "Kareem Arab",
			position: "Founder",
			bio: "Building the financial OS that consolidates fragmented wealth data through AI-powered insights.",
			image: "/generated/image-editorial-style-professional-headshot-of.webp"
		}
	]}
/>

<!-- CTA Section -->
<CallToAction
	title="Ready to see your complete financial picture?"
	subtitle="Join forward-thinking professionals"
	description="Stop wasting hours tracking scattered financial data. Get the Notion-like clarity you need to make confident wealth decisions across all your accounts."
	imageSrc="/generated/image-a-confident-professional-tech-entreprene.webp"
/>

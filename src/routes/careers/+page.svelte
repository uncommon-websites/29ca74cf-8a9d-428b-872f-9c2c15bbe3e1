<script lang="ts">
	// Types

	// Components
	import SectionHeader from "$lib/components/layout/SectionHeader.svelte";
	import Culture from "$lib/components/layout/Culture.svelte";
	import Testimonials from "$lib/components/layout/Testimonials.svelte";
	import SecondaryHero from "$lib/components/layout/hero-sections/SecondaryHero.svelte";
	import Card from "$lib/components/ui/Card.svelte";
	import JobList, { type JobOpening } from "./JobList.svelte";

	// Icons
	import IconBriefcase from "~icons/lucide/briefcase";
	import IconUsers from "~icons/lucide/users";
	import IconHeart from "~icons/lucide/heart";
	import IconGlobe from "~icons/lucide/globe";

	// Constants
	const SECTION_BASE_CLASSES = "section-py section-px container mx-auto";
	const GRADIENT_BG_CLASSES =
		"bg-gradient-to-br from-gray-50 to-gray-100 dark:from-gray-900 dark:to-gray-800";
	const ICON_CONTAINER_CLASSES =
		"bg-primary-50 text-primary-600 dark:bg-primary-950 dark:text-primary-400 flex items-center justify-center rounded-full";

	const benefits = [
  {
    title: "Global impact, real users",
    description: "Ship infrastructure that directly powers thousands of apps and millions of real users around the world.",
    icon: IconGlobe
  },
  {
    title: "Remote, flexible, and supported",
    description: "Remote-first, async work culture with flexible hours, learning budgets, and autonomy to tackle tough engineering problems.",
    icon: IconBriefcase
  },
  {
    title: "Growth and ownership",
    description: "Work with experienced founders and engineers, own critical pieces of the stack, and grow alongside a well-funded and fast-moving team.",
    icon: IconUsers
  }
];

	const openings: JobOpening[] = [
		// Engineering
		{
			title: "Senior Frontend Developer",
			department: "Engineering",
			location: "Remote",
			type: "Full-time",
			url: "#"
		},
		{
			title: "Backend Engineer",
			department: "Engineering",
			location: "Remote",
			type: "Full-time",
			url: "#"
		},
		{
			title: "Design Engineer",
			department: "Engineering",
			location: "Remote",
			type: "Full-time",
			url: "#"
		},

		// Design
		{
			title: "UX/UI Designer",
			department: "Design",
			location: "Remote",
			type: "Full-time",
			url: "#"
		},
		{
			title: "Product Designer",
			department: "Design",
			location: "Remote",
			type: "Full-time",
			url: "#"
		},

		// Product
		{
			title: "Product Manager",
			department: "Product",
			location: "Remote",
			type: "Full-time",
			url: "#"
		},
		{
			title: "Product Analyst",
			department: "Product",
			location: "Remote",
			type: "Full-time",
			url: "#"
		},

		// Marketing
		{
			title: "Marketing Specialist",
			department: "Marketing",
			location: "Remote",
			type: "Full-time",
			url: "#"
		},
		{
			title: "Content Strategist",
			department: "Marketing",
			location: "Remote",
			type: "Full-time",
			url: "#"
		},
		{
			title: "Social Media Manager",
			department: "Marketing",
			location: "Remote",
			type: "Full-time",
			url: "#"
		}
	];

	const employeeTestimonials = [
  {
    name: "Danielle Brooks",
    position: "Engineering Manager",
    company: "Platform Engineering",
    quote:
      "At Fly.io, I feel embraced for who I am. We support each other, challenge ideas, and celebrate every win together. There’s a real sense of belonging here.",
    image:
      "/generated/image-a-black-female-engineering-manager-sitti.webp"
  },
  {
    name: "Carlos Martinez",
    position: "Software Engineer I",
    company: "Web Services",
    quote:
      "My team truly invests in my growth. From day one, I’ve had mentors to learn from, space to ask questions, and the freedom to build real products that matter.",
    image:
      "/generated/image-a-latino-male-entry-level-engineer-with-.webp"
  },
  {
    name: "Alex Kim",
    position: "Product Marketing Associate",
    company: "Product & Marketing",
    quote:
      "I love that my ideas are heard. We work flexibly, move fast, and I get to see my work make a difference. People are encouraged to be themselves—every single day.",
    image:
      "/generated/image-an-asian-nonbinary-product-marketer-wear.webp"
  }
];

	const processSteps = [
  {
    step: 1,
    title: "Submit your application",
    description: "Send us your info—including experience, GitHub, blog posts, or projects that show how you work."
  },
  {
    step: 2,
    title: "Tackle a real-world challenge",
    description: "You'll do a short async technical project or code challenge that matches the work you’d do here."
  },
  {
    step: 3,
    title: "Meet the team",
    description: "Talk with our engineers or founders about your solutions, ways of working, and how we build together."
  },
  {
    step: 4,
    title: "Culture chat and offer",
    description: "Wrap up with a brief culture-fit call. We move fast—expect feedback and a decision within 1–2 weeks."
  }
];

	const values = [
  {
    icon: IconGlobe,
    title: "Remote-first, async by design",
    description: "We communicate across time zones, bias toward transparency, and support focus work—wherever you are."
  },
  {
    icon: IconHeart,
    title: "Engineer-driven decisions",
    description: "Direct access to founders, high-trust projects, and autonomy to ship infrastructure that matters."
  },
  {
    icon: IconUsers,
    title: "Open collaboration and growth",
    description: "Work in public (see our infra log!), level up with conferences and learning stipends, and help shape real world infrastructure."
  }
];
</script>

<!-- Hero Section -->

<SecondaryHero
  title="Build where it matters most"
  subtitle="Small, honest team. Fast growth, real impact, zero nonsense."
  imageSrc="/generated/image-a-diverse-group-of-people-working-togeth.webp"
/>

<!-- Why Join Us Section -->
<section class={SECTION_BASE_CLASSES}>
	<SectionHeader title="Why join us?" subtitle="Build your career while making an impact" />

	<div class="mt-16 grid gap-4 md:grid-cols-3">
		{#each benefits as benefit}
			<Card {...benefit} />
		{/each}
	</div>
</section>

<!-- Culture Section -->
<Culture {values} />

<Testimonials testimonials={employeeTestimonials} />

<!-- Application Process -->
<section class={SECTION_BASE_CLASSES}>
	<div class="mx-auto">
		<h2 class="text-title1 mb-16">Our application process</h2>

		<div class="grid gap-12 md:grid-cols-3">
			{#each processSteps as { step, title, description }, i}
				<div class="flex flex-col">
					<div class="{ICON_CONTAINER_CLASSES} mb-6 size-11">
						<span class="text-headline">{step}</span>
					</div>
					<h3 class="text-headline mb-3">{title}</h3>
					<p class="text-body text-emphasis-low">{description}</p>
				</div>
			{/each}
		</div>
	</div>
</section>
<!-- Current Openings Section -->
<section class={GRADIENT_BG_CLASSES}>
	<div class="section-px section-py container mx-auto grid w-full items-start lg:grid-cols-2">
		<SectionHeader title="Current openings" subtitle="Find your perfect role" />

		<JobList {openings} />
	</div>
</section>

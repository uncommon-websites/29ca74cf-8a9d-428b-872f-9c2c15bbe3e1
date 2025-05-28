<script lang="ts">
	// Types
	import type { PageProps } from "./$types";

	// Components
	import Features from "$lib/components/layout/Features.svelte";
	import Testimonials from "$lib/components/layout/Testimonials.svelte";
	import CallToAction from "$lib/components/layout/CallToAction.svelte";
	import Pricing from "$lib/components/layout/Pricing.svelte";

	// Props
	const { data }: PageProps = $props();
</script>

<Pricing />

<Testimonials
  testimonials={[
    {
      name: "Anisa Denton",
      position: "CTO",
      company: "Tigris",
      quote:
        "We reduced p99 latency by over 80% moving to Fly.io, and our app’s responsiveness unlocked growth we couldn’t achieve before.",
      image:
        "/generated/image-a-professional-headshot-of-a-black-briti.webp",
    },
    {
      name: "Luis Marques",
      position: "Engineering Lead",
      company: "Glide",
      quote:
        "Ship-to-prod is faster, our infrastructure is simpler, and we haven’t had to touch Kubernetes once.",
      image:
        "/generated/image-a-professional-headshot-of-a-portuguese-.webp",
    },
    {
      name: "Eamon Scott",
      position: "Platform Engineer",
      company: "SavvyCal",
      quote:
        "Managed Postgres on Fly was the easiest database setup I’ve ever done. It just worked, even globally.",
      image:
        "/generated/image-a-professional-headshot-of-an-irish-man-.webp",
    },
  ]}
/>

<CallToAction
  title="Run your app where your users are"
  subtitle="Deploy globally in seconds with no vendor lock-in, fast boot times, and pay-as-you-go pricing."
  description="See how fast teams move on Fly.io—real support, simple setup, free to get started."
  imageSrc="/generated/image-a-cheerful-developer-sitting-at-a-wooden.webp"
  callsToAction={[
    {
      href: "/start",
      label: "Get started free",
      variant: "primary"
    },
    {
      href: "/contact",
      label: "Contact sales",
      variant: "secondary"
    }
  ]}
/>

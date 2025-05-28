<script lang="ts">
	// Components
	import UseCases from "$lib/components/layout/UseCases.svelte";
	import Summary from "$lib/components/layout/Summary.svelte";
	import Features from "$lib/components/layout/Features.svelte";
	import Testimonials from "$lib/components/layout/Testimonials.svelte";
	import CallToAction from "$lib/components/layout/CallToAction.svelte";
	import AboutTeaser from "$lib/components/layout/AboutTeaser.svelte";
	import LogoScroller from "$lib/components/layout/LogoScroller.svelte";
	import CustomerCardHero from "$lib/components/layout/hero-sections/CustomerCardHero.svelte";
</script>

<CustomerCardHero
  centered={true}
  title="Deploy globally. Run instantly."
  subtitle="Fly.io runs your app close to users for fast startups, low latency, and high uptime—anywhere in the world."
  customers={[
    {
      name: "Alicia Park",
      position: "Lead backend engineer, Syncster",
      imageSrc: "/generated/image-a-korean-woman-software-engineer-in-a-li.webp"
    },
    {
      name: "Mateo Garcia",
      position: "CTO, Libra Analytics",
      imageSrc: "/generated/image-a-latino-man-cto-in-a-modern-open-plan-o.webp"
    },
    {
      name: "Priya Deshmukh",
      position: "Senior platform engineer, Kitewave",
      imageSrc: "/generated/image-an-indian-woman-platform-engineer-at-her.webp"
    },
    {
      name: "Liam Chen",
      position: "Head of infrastructure, Glint",
      imageSrc: "/generated/image-a-chinese-man-it-leader-in-a-data-center.webp"
    },
    {
      name: "Nia Johnson",
      position: "Staff developer, Flexstage",
      imageSrc: "/generated/image-a-black-woman-developer-in-an-urban-offi.webp"
    }
  ]}
/>

<LogoScroller 
	label="Trusted by industry leaders"
	logoUrls={[
		'https://logo.clearbit.com/supabase.com',
		'https://logo.clearbit.com/tailscale.com',
		'https://logo.clearbit.com/upstash.com',
		'https://logo.clearbit.com/tigrisdata.com'
	]}
/>

<Summary
	title="What we do"
	text="Fly.io lets you deploy apps, APIs, and databases to fast, isolated micro-VMs around the world. Run workloads close to your users for lower latency, better performance, and less complexity. Pay only for what you use."
/>

<Testimonials
	testimonials={[
		{
			name: "Cormac Reyes",
			position: "Principal Engineer",
			company: "Alpine Bay",
			quote: "With Fly.io, we dropped deploy time from 20 minutes to under 90 seconds. No pipelines. No region-specific tweaks. The Machines API got us global fast without the pain.",
			image: "/generated/image-a-finnish-man-software-engineer-in-a-mod.webp"
		},
		{
			name: "Mae Levin",
			position: "Senior Platform Engineer",
			company: "Oakframe Systems",
			quote: "We had a region go dark at 3am—and our app kept humming. Fly.io's global failover and request routing handled it. No pager alerts. No lost traffic.",
			image: "/generated/image-a-brazilian-woman-site-reliability-engin.webp"
		},
		{
			name: "Ezra Kwan",
			position: "DevOps Lead",
			company: "SegmentRoll",
			quote: "Using Fly.io, we brought infra costs down 38% in Q1 just by shifting workloads to scale-to-zero Machines and pulling Postgres in-region. Running smart is finally easy.",
			image: "/generated/image-a-turkish-man-cto-on-a-call-in-a-tech-co.webp"
		}
	]}
/>

<Features
	title="What makes Fly.io different"
	subtitle="Six core features for builders and teams"
	features={[
		{
			title: "Fast-launching VMs anywhere",
			description: "Fly Machines boot in milliseconds and run Docker containers on demand in over 35 regions."
		},
		{
			title: "Run apps close to your users",
			description: "Route traffic to the nearest healthy instance with global Anycast networking for low latency worldwide."
		},
		{
			title: "Stateful workloads that scale",
			description: "Attach persistent NVMe storage or use managed Postgres, LiteFS Cloud for SQLite, and Upstash Redis—replicated globally."
		},
		{
			title: "Simple networking, powerful routing",
			description: "Get private networking (WireGuard), granular control of request routing, and static egress IPs for every machine."
		},
		{
			title: "Inference-ready infrastructure",
			description: "Deploy GPU machines for AI/ML inference, real-time streaming, and LLMs in North America and Europe."
		},
		{
			title: "Usage-based billing, no surprises",
			description: "Pay only for what you use, with scale-to-zero, machine reservations, and accidental deployment forgiveness."
		}
	]}
/>

<UseCases
	title="Use Cases"
	subtitle="Real-world applications for your business needs"
	useCases={[
		{
			title: "Global app deployment for real-time experiences",
			description: "Deploy your app in multiple regions so users always connect to the nearest instance. Great for real-time APIs, multiplayer games, and fully interactive UIs with authentication, caching, and session storage at the edge.",
			image: "/generated/image-a-diverse-group-of-remote-developers-col.webp",
			link: {
				href: "/use-cases/globalapp",
				label: "Learn more"
			}
		},
		{
			title: "Reliable SaaS and databases at global scale",
			description: "Run applications and critical databases near your customers without losing consistency. With Fly Volumes, LiteFS Cloud, and Managed Postgres, you can build and run full-featured multi-region SaaS—without needing to be a distributed systems expert.",
			image: "/generated/image-an-engineering-team-working-together-to-.webp",
			link: {
				href: "/use-cases/globalsaas",
				label: "Learn more"
			}
		},
		{
			title: "AI inference and LLMs close to users",
			description: "Launch AI inference workloads on GPU-accelerated Fly Machines anywhere in our global network. Reduce inference latency, keep cloud costs predictable, and spin down idle workloads with scale-to-zero.",
			image: "/generated/image-a-machine-learning-engineer-collaboratin.webp",
			link: {
				href: "/use-cases/aiinference",
				label: "Learn more"
			}
		}
	]}
/>

<AboutTeaser />
<CallToAction 
  title="Ship applications that just feel faster"
  subtitle="Deploy globally, scale instantly, pay only for what you use"
  description="Launch your app or database close to your users around the world with Fly.io. Micro-VMs start in milliseconds—and you only pay while your code is running."
  imageSrc="/generated/image-a-cheerful-developer-sitting-at-a-desk-i.webp"
  callsToAction={[{ href: '/get-started', label: 'Try Fly.io', variant: 'primary' }]}
/>

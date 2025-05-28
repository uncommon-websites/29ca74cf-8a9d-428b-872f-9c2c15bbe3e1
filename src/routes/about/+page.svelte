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
    title: "Radical transparency",
    description: "We share incident logs, publish engineering deep-dives, and admit mistakes out loud."
  },
  {
    title: "Everyone ships",
    description: "From founders to new hires, everyone writes code and makes technical decisions."
  },
  {
    title: "Bias for action",
    description: "We ship features, fix bugs fast, and let developers own their projects."
  },
  {
    title: "Direct support",
    description: "Engineers help customers directly—we don’t hide behind support layers."
  },
  {
    title: "Low ego, high standards",
    description: "We debate hard, but egos stay checked. It’s about the work, not titles."
  }
];
</script>

<SecondaryHero
    title="Run apps everywhere, instantly"
    subtitle="Fast global infrastructure, built for your CLI"
    imageSrc="/generated/image-a-diverse-team-of-professionals-working-.webp"
/>

<!-- Story Section -->
<Story
	paragraphs={[
		"We started Fly.io because we were tired of the same story: smart developers building great web apps, only to be slowed down by slow clouds, complicated deployment pipelines, and the distance between users and infrastructure. As engineers who’ve spent years building software and working on internet infrastructure, we knew developers deserved better tools to run apps globally—without needing an ops team or playing cloud maze-chase.",
		"So we built a platform that makes it easy to run full-stack apps and their databases right where your users are—anywhere in the world. Fly.io uses fast-booting micro-VMs to run containerized apps with minimal cold start time, has a global Anycast backbone to route requests instantly, and offers local NVMe-backed volumes to keep data close and performance tight. From the beginning, we focused on giving developers a simple yet powerful CLI-first experience through flyctl, because we use terminals too, and clicking through hidden settings is nobody’s idea of fun.",
		"Today, teams building everything from Rails monoliths to Elixir LiveView apps, Laravel backends, AI inference services, and multi-region databases are using Fly.io to ship more, scale globally, and worry less. We’re trusted by startups and companies like Supabase, Tailscale, and Mailgun. If your users are everywhere, your app should be too—and Fly.io makes that possible in minutes, straight from your terminal."
	]}
/>

<!-- Our Culture Section -->
<Culture {values} />

<!-- StakeholderGrid Section -->
<StakeholderGrid
  stakeholderType="team"
  title="Our founders."
  subtitle="Engineered by developers for developers."
  stakeholders={[
    {
      name: "Kurt Mackey",
      position: "Co-founder & CEO",
      bio: "Kurt leads Fly.io with a focus on developer experience, CLI-first workflows, and making global infrastructure simple for teams of all sizes.",
      image: "/generated/image-a-headshot-of-a-male-founder-in-a-studio.webp"
    },
    {
      name: "Thomas Ptacek",
      position: "Co-founder",
      bio: "Thomas designs the core systems security and networking at Fly.io, ensuring reliability, performance, and deep transparency for our users.",
      image: "/generated/image-a-headshot-of-a-male-founder-wearing-gla.webp"
    },
    {
      name: "Jerome Gravel-Niquet",
      position: "Co-founder",
      bio: "Jerome builds Fly.io's stateful infrastructure—volumes, storage, and distributed data—powering databases and persistent workloads everywhere.",
      image: "/generated/image-a-headshot-of-a-male-founder-with-a-bear.webp"
    }
  ]}
/>

<StakeholderGrid
	stakeholderType="investor"
	title="Backed by the best."
	subtitle="Point Nine, TSIC and others"
	stakeholders={[
		{
			name: "Point Nine Capital",
			image: "https://cdn.brandfetch.io/pointnine.com/w/400/h/400/logo?c=1id_elLz2Bd5Ej-dWo7"
		},
		{
			name: "TSIC Ventures",
			image: "https://cdn.brandfetch.io/tiny.vc/w/400/h/400/logo?c=1a2b3c4d5e"
		},
		{
			name: "Sequoia Capital",
			image: "https://cdn.brandfetch.io/sequoiacap.com/w/400/h/400/logo"
		}
	]}
/>

<!-- CTA Section -->
<CallToAction
  title="Help build the world's developer cloud"
  subtitle="Join us at Fly.io"
  description="Fly.io is a team of builders, not buzzword collectors. You'll ship real infrastructure, work directly with smart developers, and solve hard problems every week. Curious? See our open roles or just start a conversation."
  callsToAction={[{ href: '/careers', label: 'See open roles', variant: 'primary' }, { href: '/contact', label: 'Say hello', variant: 'secondary' }]}
/>

<script>
	import * as m from '$lib/paraglide/messages.js';
	import { getLocale, setLocale } from '$lib/paraglide/runtime.js';
	import richard from '$lib/assets/testimonials/richard.jpg';

	import Testimonial from './components/Testimonial.svelte';
	import Hero from './components/Hero.svelte';
	import ReadAboutUs from './components/ReadAboutUs.svelte';
	import Integration from './components/Integration.svelte';
	import Benefits from './components/Benefits.svelte';
	import UseCases from './components/UseCases.svelte';
	import Pricing from './components/Pricing.svelte';
	import Cta from './components/CTA.svelte';
</script>

<svelte:head>
	<title>Nexara</title>
	<meta name="description" content={m.meta_nexara()} />
	<meta
		name="keywords"
		content="Speech-to-text, Speech-to-text API, automations, n8n, transcription, transcription API, transcription service, transcription software, transcription software for automations, transcription software for n8n"
	/>
	<meta property="og:title" content="Nexara" />
	<meta
		property="og:description"
		content="Effortless speech-to-text for your no-code workflows. Easy integration with n8n."
	/>
	<meta property="og:type" content="website" />
	<meta property="og:url" content="https://www.nexara.ru/" />
	<meta property="og:locale" content={getLocale() === 'ru' ? 'ru_RU' : 'en_US'} />
	<link rel="preconnect" href="https://fonts.googleapis.com" />
	<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
	<link
		href="https://fonts.googleapis.com/css2?family=Fira+Code:wght@300..700&family=Golos+Text:wght@400..900&display=swap"
		rel="stylesheet"
	/>
</svelte:head>

<Hero></Hero>
<Testimonial text={m.testimonial_richard()} subtitle={m.testimonial_richard_name()} image={richard}
></Testimonial>
<Integration></Integration>
<Benefits></Benefits>
<UseCases></UseCases>
<Pricing></Pricing>

{#if getLocale() === 'ru'}
	<ReadAboutUs></ReadAboutUs>
{/if}

<Cta></Cta>

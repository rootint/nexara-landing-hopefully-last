<script>
	import * as m from '$lib/paraglide/messages.js';
	import { getLocale, setLocale } from '$lib/paraglide/runtime.js';
</script>

<section class="hero">
	<div class="minutes-badge">
		<p class="minutes-badge-text">{m.hero_minutes()}</p>
	</div>
	<div class="hero-content">
		<h1 class="hero-title">{m.hero_title()}</h1>
		<h2 class="hero-subtitle">{m.hero_subtitle()}</h2>
	</div>
	<div class="buttons">
		<a href={getLocale() === 'ru' ? 'https://app.nexara.ru' : 'https://app.nexara.ru/en'}>
			<button class="hero-main-button">{m.hero_main_button()}</button>
		</a>
		<a
			target="_blank"
			rel="noopener noreferrer"
			href={getLocale() === 'ru'
				? 'https://docs.nexara.ru/ru/n8n-guide'
				: 'https://docs.nexara.ru/en/n8n-guide'}
		>
			<button class="hero-secondary-button">{m.hero_secondary_button()}</button>
		</a>
	</div>
</section>

<style>
	.hero-main-button {
		background-color: var(--text);
		color: var(--bg);
		font-size: 20px;
		padding: 16px 40px;
	}
	.hero-main-button:hover {
		background-color: var(--text-2);
	}
	.hero-secondary-button {
		background-color: var(--bg-button);
		color: var(--text);
		font-size: 20px;
		padding: 16px 40px;
		border: 1px solid var(--border);
		backdrop-filter: blur(16px);
	}
	.hero-secondary-button:hover {
		background-color: var(--bg-elevation-1);
	}

	.buttons {
		display: flex;
		gap: 36px;
		flex-direction: row;
		align-items: center;
		justify-content: center;
		animation: fadeIn 1s ease;
	}

	.hero-content {
		display: flex;
		flex-direction: column;
		align-items: center;
		justify-content: center;
		animation: simpleFadeIn 0.7s ease;
	}
	.hero-title {
		text-align: center;
		max-width: 860px;
		margin-top: 24px;
		margin-bottom: 36px;
		color: var(--text);
		line-height: 135%;
	}

	.hero-subtitle {
		font-size: 24px;
		max-width: 680px;
		text-align: center;
		font-weight: 400;
		margin-bottom: 64px;
		line-height: 140%;
	}
	.minutes-badge {
		padding: 12px 20px;
		border-radius: 12px;
		background-color: var(--bg-elevation-1);
		border: 1px solid var(--border);
		animation: simpleFadeIn 0.7s ease;
		backdrop-filter: blur(16px);
	}

	.minutes-badge-text {
		color: var(--text);
		font-size: 16px;
		text-align: center;
	}
	.hero {
		display: flex;
		flex-direction: column;
		align-items: center;
		justify-content: center;
		margin: 0 auto;
		min-height: 860px;
		padding-top: 72px;
		position: relative;
	}
</style>

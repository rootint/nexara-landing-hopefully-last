<script>
	import icon from '$lib/assets/icon.png';
	import * as m from '$lib/paraglide/messages.js';
	import { getLocale, setLocale } from '$lib/paraglide/runtime.js';

	function switchLanguage() {
		const currentLocale = getLocale();
		const nextLocale = currentLocale === 'ru' ? 'en' : 'ru';
		setLocale(nextLocale);
	}

	/**
	 * Reactive declaration for the button text.
	 * Shows the language code the button will switch *to*.
	 */
	$: targetLanguageCode = getLocale() === 'ru' ? 'EN' : 'RU';
</script>

<header>
	<nav>
		<div class="top-row">
			<img src={icon} width="21" alt="logo" />
			<div style="width: 12px" />
			<p class="logo">Nexara</p>
		</div>
		<div class="top-row">
			<div class="hide-on-mobile">
				<a
					href={getLocale() === 'ru'
						? 'https://docs.nexara.ru/ru/quickstart'
						: 'https://docs.nexara.ru/en/quickstart'}><p>{m.header_docs()}</p></a
				>
				<div style="width: 4rem" />
				<a
					href={getLocale() === 'ru'
						? 'https://discord.gg/wuj8dwQKrv'
						: 'https://discord.gg/wuj8dwQKrv'}><p>Discord</p></a
				>
				<div style="width: 4rem" />
				<!-- Fancy Language Switch Button -->
				<!-- <button class="lang-switch-btn" on:click={switchLanguage} title="Switch Language">
					{targetLanguageCode}
				</button> -->
				<!-- <div style="width: 4rem" /> -->
				<!-- End Language Switch Button -->

				<a href={getLocale() === 'ru' ? 'https://app.nexara.ru' : 'https://app.nexara.ru/en'}>
					<button class="cta-btn">
						<div class="row">
							<!-- {/* TODO: Use Paraglide messages for i18n: <p class="button-text">{m.login()}</p> */} -->
							<p class="button-text">{m.header_login()}</p>
						</div>
					</button>
				</a>
			</div>
			<div class="show-on-mobile">
				<button class="lang-switch-btn" on:click={switchLanguage} title="Switch Language">
					{targetLanguageCode}
				</button>
			</div>
		</div>
	</nav>
</header>

<style>
	/* Existing styles */
	.cta-btn {
		background-color: #fff;
		padding: 8px 20px;
		border-radius: 12px;
		border: none;
		cursor: pointer;
		transition: background-color 0.3s ease; /* Added transition */
	}
	.button-text {
		color: #111;
	}

	/* Removed dropdown styles */
	/* .language-selector { ... } */
	/* .lang-toggle-btn { ... } */
	/* .lang-dropdown { ... } */
	/* .lang-option { ... } */

	/* New Fancy Language Switch Button Styles */
	.lang-switch-btn {
		background: transparent; /* Clear background */
		border: 1px solid rgba(255, 255, 255, 0.6); /* Slightly transparent white border */
		color: #fff;
		padding: 8px 16px; /* Adjust padding if needed */
		border-radius: 8px;
		cursor: pointer;
		font-weight: 500; /* Slightly bolder */
		font-size: 0.9rem; /* Slightly smaller */
		min-width: 55px; /* Ensure enough space for RU/EN */
		text-align: center;
		transition: all 0.3s ease; /* Smooth transition for hover effects */
		box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1); /* Subtle shadow */
	}

	/* End New Button Styles */

	.go-home {
		text-decoration: none;
	}
	.show-on-mobile {
		display: none;
	}
	.logo {
		font-weight: 400;
	}
	a {
		text-decoration: none;
		font-weight: 300;
		color: inherit; /* Ensure links inherit nav color */
	}
	a p {
		transition: color 0.2s ease; /* Smooth color transition for links */
	}
	a:hover p {
		color: #ccc; /* Slightly lighter color on hover for links */
	}
	.hide-on-mobile {
		display: flex;
		align-items: center;
	}
	@media (max-width: 768px) {
		.hide-on-mobile {
			display: none;
		}
	}
	nav {
		color: #fff;
		display: flex;
		justify-content: space-between;
		align-items: center;
		margin: 0; /* Removed horizontal margin */
		margin-top: 32px;
		font-weight: 300;
		position: absolute;
		left: 24px;
		top: 0;
		right: 24px;
		animation: simpleFadeIn 0.7s ease;
		z-index: 100;
	}

	@media (max-width: 768px) {
		nav {
			/* color: #fff; Inherited */
			display: flex;
			justify-content: space-between;
			align-items: center;
			margin: 0; /* Reset margin */
			padding: 16px 24px 0 24px; /* Add padding instead of relying on absolute positioning margins */
			position: static; /* Let it flow normally on mobile */
			animation: none; /* Disable fade-in on mobile if desired */
		}
		.show-on-mobile {
			display: flex;
			align-items: center; /* Align items */
			gap: 1.5rem; /* Add space between mobile links */
		}
		.show-on-mobile a p {
			font-size: 0.9rem; /* Slightly smaller text on mobile */
		}
	}

	.top-row {
		display: flex;
		align-items: center;
	}

	p {
		font-weight: 400;
		font-size: 1rem;
		margin: 0; /* Remove default paragraph margin */
	}
</style>

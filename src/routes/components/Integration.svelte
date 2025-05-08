<script>
	import { Computer } from 'lucide-svelte';
	import { m } from '$lib/paraglide/messages';
</script>

<section class="integration">
	<h2>{m.integration_title()}</h2>
	<p class="integration-subtitle">{m.integration_subtitle()}</p>
	<div class="cards">
		<div class="card">
			<Computer size="32"></Computer>
			<h3 class="card-title">Get your API key</h3>
			<p class="card-desc">Register on the Nexara dashboard to grab your API key.</p>
			<p class="bg-number">1</p>
		</div>
		<div class="card">
			<Computer size="32"></Computer>
			<h3 class="card-title">Configure</h3>
			<p class="card-desc">
				Add an HTTP Request node in n8n, import our quick cURL command, and link your audio file.
			</p>
			<p class="bg-number">2</p>
		</div>
		<div class="card">
			<Computer size="32"></Computer>
			<h3 class="card-title">Transcribe!</h3>
			<p class="card-desc">Run your workflow – Nexara delivers your transcript automatically.</p>
			<p class="bg-number">3</p>
		</div>
	</div>
</section>

<style>
	.card {
		flex: 1 0 300px;
	}
	.cards {
		display: flex;
		flex-wrap: wrap;
		gap: 32px;
		margin-top: 48px;
	}
	.bg-number {
		position: absolute;
		font-size: 40px;
		font-weight: 450;
		color: var(--border);
		right: 32px;
		top: 20px;
	}
	.card-title {
		margin-top: 32px;
		margin-bottom: 20px;
		font-size: 24px;
		text-align: start;
		color: var(--text);
		font-weight: 480;
	}
	.card-desc {
		line-height: 140%;
		font-size: 16px;
		margin: 0;
		text-align: start;
		padding: 0;
		color: var(--text-2);
	}
	.integration {
		margin-top: 172px;
		display: flex;
		flex-direction: column;
		align-items: center;
		justify-content: center;
	}
	.integration-subtitle {
		font-size: 20px;
		text-align: center;
		font-weight: 400;
		color: var(--text-2);
	}
</style>

<script>
	import { GraduationCap, Headset, Globe, AudioLines } from 'lucide-svelte';
	import { m } from '$lib/paraglide/messages';
	import { getLocale, setLocale } from '$lib/paraglide/runtime.js';
</script>

<section class="usage" id="for-who">
	<h2>{m.usage_title()}</h2>
	<h3>{m.usage_subtitle()}</h3>
	<div class="cards">
		<div class="card">
			<Headset size="32"></Headset>
			<h3 class="card-title">{m.usage_step1_title()}</h3>
			<p class="card-desc">
				{m.usage_step1_subtitle()}
			</p>
		</div>
		<div class="card">
			<Globe size="32"></Globe>
			<h3 class="card-title">{m.usage_step2_title()}</h3>
			<p class="card-desc">
				{m.usage_step2_subtitle()}
			</p>
		</div>
		<div class="card">
			<AudioLines size="32"></AudioLines>
			<h3 class="card-title">{m.usage_step3_title()}</h3>
			<p class="card-desc">
				{m.usage_step3_subtitle()}
			</p>
		</div>
	</div>
</section>

<style>
	.cards {
		display: flex;
		flex-wrap: wrap;
		gap: 32px;
		margin-top: 48px;
	}
	.card-title {
		margin-top: 32px;
		margin-bottom: 20px;
		font-size: 24px;
		text-align: start;
		color: #fff;
		font-weight: 480;
	}
	.card-desc {
		line-height: 145%;
		font-size: 16px;
		margin: 0;
		text-align: start;
		padding: 0;
		color: var(--text-2);
	}
	.card {
		flex: 1 0 300px;
	}
	.usage {
		display: flex;
		flex-direction: column;
		margin-top: 128px;
	}

	@media (max-width: 768px) {
		.usage {
			display: flex;
			flex-direction: column;
			margin-top: 72px !important;
		}
	}
</style>

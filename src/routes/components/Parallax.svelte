<script>
	import green from '$lib/assets/bg/green.svg';
	import orange from '$lib/assets/bg/orange.svg';
	import red from '$lib/assets/bg/red.svg';
	import purple from '$lib/assets/bg/purple.svg';

	let scrollPosition = 0;
</script>

<div class="parallax-container">
	<img id="green" src={green} width="794" style="transform: rotateZ({scrollPosition / 90}deg)" />
	<img id="red" src={red} width="547" style="transform: rotateZ({scrollPosition / 90}deg)" />
	<img id="orange" src={orange} width="685" style="transform: rotateZ({-scrollPosition / 90}deg)" />
	<img id="purple" src={purple} width="794" style="transform: rotateZ({scrollPosition / 90}deg)" />
</div>

<style>
	#green {
		right: -600px;
		bottom: -300px;
	}
	#red {
		top: -400px;
		left: 20%;
	}
	#orange {
		bottom: 0px;
		left: -500px;
	}
	#purple {
		right: -350px;
		top: 10px;
	}
	.parallax-container {
		position: fixed;
		height: 100vh;
		width: 100vw;
		animation: simpleFadeIn 0.7s ease;
		overflow: hidden;
	}
	img {
		transform: translate3d(0px, 0px, 0px) scale3d(1, 1, 1) rotateX(0deg) rotateY(0deg) rotateZ(0deg)
			skew(0deg, 0deg);
		transform-style: preserve-3d;
		position: absolute;
	}
</style>

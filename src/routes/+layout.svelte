<script>
	import './styles.css';
	import Parallax from './components/Parallax.svelte';
	import Footer from './components/Footer.svelte';
	import Header from './components/Header.svelte';
</script>

<Parallax></Parallax>

<div class="app">
	<Header></Header>
	<main>
		<slot />
	</main>
</div>
<footer>
	<!-- <Footer></Footer> -->
</footer>

<style>
	footer {
		position: relative;
		z-index: 100;
		padding: 32px;
		box-sizing: border-box;
		background-color: var(--bg-elevation-1);
		backdrop-filter: blur(16px);
		transform: translate3d(0px, 0px, 0px) scale3d(1, 1, 1) rotateX(0deg) rotateY(0deg) rotateZ(0deg)
			skew(0deg, 0deg);
		transform-style: preserve-3d;
		display: flex;
		justify-content: center;
	}
</style>

<script lang="ts">
	export let name: string;
	import ImageLoader from './components/Image/ImageLoader.svelte';

	// Generate random number to stop the images caching
	function rand(min, max) {
		let randomNum = Math.random() * (max - min) + min;
		return Math.round(randomNum);
	}
</script>

<style>
	main {
		text-align: center;
		padding: 1em;
		max-width: 240px;
		margin: 0 auto;
	}

	h1 {
		color: #ff3e00;
		text-transform: uppercase;
		font-size: 4em;
		font-weight: 100;
	}

	li {
		list-style: none;
		background: #eee;
		width: 200px;
		height: 200px;
		margin: 2em;
	}

	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}
</style>

<main>
	<h1>{name}!</h1>
	<h2>Image lazy load</h2>
	<ul>
		<li><ImageLoader src={`https://picsum.photos/seed/${rand(0,200)}/800/800`} alt="Example image" /></li>
		<li><ImageLoader src={`https://picsum.photos/seed/${rand(0,200)}/800/800`} alt="Example image" /></li>
		<li><ImageLoader src={`https://picsum.photos/seed/${rand(0,200)}/800/800`} alt="Example image" /></li>
		<li><ImageLoader src={`https://picsum.photos/seed/${rand(0,200)}/800/800`} alt="Example image" /></li>
		<li><ImageLoader src={`https://picsum.photos/seed/${rand(0,200)}/800/800`} alt="Example image" /></li>
		<li><ImageLoader src={`https://picsum.photos/seed/${rand(0,200)}/800/800`} alt="Example image" /></li>
		<li><ImageLoader src={`https://picsum.photos/seed/${rand(0,200)}/800/800`} alt="Example image" /></li>
		<li><ImageLoader src={`https://picsum.photos/seed/${rand(0,200)}/800/800`} alt="Example image" /></li>
		<li><ImageLoader src={`https://picsum.photos/seed/${rand(0,200)}/800/800`} alt="Example image" /></li>
		<li><ImageLoader src={`https://picsum.photos/seed/${rand(0,200)}/800/800`} alt="Example image" /></li>
	</ul>
</main>

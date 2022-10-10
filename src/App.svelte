<script lang="ts">
	import ReactivityButton from './chap2/Reactivity.svelte';
	import ArraysAndObjects from './chap2/ArraysAndObjects.svelte';

	let name: string;
	name = 'me'
</script>

<main>
	<h1>Hello {name}!</h1>
	<h3> Chap 2. Reactivity </h3>
	<div class="chap2-root">
		<ReactivityButton />
		<ArraysAndObjects />
	</div>
</main>

<style>
	main {
		text-align: center;
		padding: 1em;
		max-width: 240px;
		margin: 0 auto;
	}

	h1 {
		color: #ff3e00;
		font-size: 4em;
		font-weight: 100;
	}

	.chap2-root {
		align-items: center;
	}

	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}
</style>
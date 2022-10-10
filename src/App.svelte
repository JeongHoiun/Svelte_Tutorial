<script lang="ts">
	import ReactivityButton from './chap2/Reactivity.svelte';
	let name: string;
	name = 'me'
</script>

<main>
	<h1>Hello {name}!</h1>
	<ReactivityButton />
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

	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}
</style>
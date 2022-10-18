<script lang="ts">
	import ReactivityButton from './chap2/Reactivity.svelte';
	import ArraysAndObjects from './chap2/ArraysAndObjects.svelte';
	import ChapThree from './chap3/index.svelte';
	import IfBlocks from './chap4/IfBlocks.svelte';
	import IfElseBlocks from './chap4/IfElseBlocks.svelte';
	import EachBlocks from './chap4/EachBlocks.svelte';
	import KeyingEach from './chap4/KeyingEach.svelte';
	import AwaitBlocks from './chap4/AwaitBlocks.svelte';
	import EventModifier from './chap5/EventModifier.svelte';
	import ComponentEvent from './chap5/ComponentEvent.svelte'
	import TextBinding from './chap6/TextBinding.svelte'
	import GroupBinding from './chap6/GroupBinding.svelte'
	import MediaBinding from './chap6/MediaBinding.svelte'
	import ComponentBinding from './chap6/ComponentBinding.svelte'
	let name: string;
	name = 'me';
</script>

<main>
	<h1>Hello {name}!</h1>
	<h3> Chap 2. Reactivity </h3>
	<div class="chap2-root">
		<ReactivityButton />
		<ArraysAndObjects />
	</div>
	<h3> Chap 3. Props </h3>
	<div>
		<ChapThree />
	</div>
	<h3> Chap 4. Logics </h3>
	<div>
		<IfBlocks />
		<IfElseBlocks/>
		<EachBlocks/>
		<KeyingEach/>
		<AwaitBlocks/>
	</div>
	<h3> Chap 5. Event </h3>
	<div>
		<EventModifier />
		<ComponentEvent />
	</div>
	<h3> Chap 6. Binding </h3>
	<div>
		<TextBinding />
		<GroupBinding/>
		<MediaBinding/>
		<ComponentBinding/>
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
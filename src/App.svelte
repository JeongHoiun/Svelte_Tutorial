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
	import LifecycleOnMount from './chap7/LifecycleOnMount.svelte'
	import Eliza from './chap7/Eliza.svelte'
	import Tick from './chap7/Tick.svelte'
	import Writablestore from './chap8/App.svelte'
	import Tweened from './chap9/Tweened.svelte'
	import Spring from './chap9/Spring.svelte'
	import TransitionDirective from './chap10/TransitionDirective.svelte'
	import TransitionParams from './chap10/TransitionParams.svelte'
	import InAndOut from './chap10/InAndOut.svelte'
	import CustomTransition from './chap10/CustomTransition.svelte'
	import KeyBlock from './chap10/KeyBlock.svelte'
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
	<h3> Chap 7. Lifecycle </h3>
	<div>
		<LifecycleOnMount />
		<Eliza/>
		<Tick/>
	</div>
	<h3> Chap 8. Stores </h3>
	<div>
		<Writablestore />
	</div>
	<h3> Chap 9. Motions</h3>
	<div>
		<Tweened/>
		<Spring/>
	</div>
	<h3> Chap 10. Transition </h3>
	<div>
		<TransitionDirective/>
		<TransitionParams/>
		<InAndOut/>
		<CustomTransition/>
		<KeyBlock/>
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
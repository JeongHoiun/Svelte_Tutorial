<script>
	import Nested from './Nested.svelte';
	import Info from './Info.svelte';

	const pkg = {
		name: 'svelte',
		version: 3,
		speed: 'blazing',
		website: 'https://svelte.dev'
	};
</script>

<Nested answer={42}/>
<Nested/>

<Info {...pkg}/>
<script>
	let current = 'foo';
	let bgOpacity = 0.5;
	$: color = bgOpacity < 0.6 ? '#000' : '#fff';
</script>

<button
	class:selected="{current === 'foo'}"
	on:click="{() => current = 'foo'}"
>foo</button>

<button
	class:selected="{current === 'bar'}"
	on:click="{() => current = 'bar'}"
>bar</button>

<button
	class:selected="{current === 'baz'}"
	on:click="{() => current = 'baz'}"
>baz</button>


<input type="range" min="0" max="1" step="0.1" bind:value={bgOpacity} />

<p style:color style:--opacity={bgOpacity}>This is a paragraph.</p>

<style>
	button {
		display: block;
	}

	.selected {
		background-color: #ff3e00;
		color: white;
	}

	p {
		font-family: "Comic Sans MS", cursive;
		background: rgba(255, 62, 0, var(--opacity));
	}
</style>

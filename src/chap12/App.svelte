<script>
    import { clickOutside } from "./click_outside.js";
	import { longpress } from './longpress.js';

	let pressed = false;
	let duration = 2000;
	
	let showModal = true;
</script>

<button on:click={() => (showModal = true)}>Show Modal</button>
{#if showModal}
	<div class="box" use:clickOutside on:outclick="{() => (showModal = false)}">
		Click outside me!
	</div>
{/if}
<label>
	<input type=range bind:value={duration} max={2000} step={100}>
	{duration}ms
</label>

<button use:longpress={duration}
	on:longpress="{() => pressed = true}"
	on:mouseenter="{() => pressed = false}"
>press and hold</button><!--mouseenter는 기본 DOM event handler-->

{#if pressed}
	<p>congratulations, you pressed and held for {duration}ms</p>
{/if}

<style>
	.box {
		--width: 100px;
		--height: 100px;
		width: var(--width);
		height: var(--height);
		left: calc(50% - var(--width) / 2);
		top: calc(50% - var(--height) / 2);
		display: flex;
		align-items: center;
		padding: 8px;
		border-radius: 4px;
		background-color: #ff3e00;
		color: #fff;
		text-align: center;
		font-weight: bold;
	}
</style>

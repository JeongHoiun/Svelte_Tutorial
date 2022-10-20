<script>
    import { onMount } from 'svelte'
	let users = [];

    onMount(async () => {
		const res = await fetch(`/account/`);
		users = await res.json();
	})
</script>

<div class="photos">
	{#each users as user}
    <p>user</p>
	{:else}
		<p>loading...</p>
	{/each}
</div>

<style>
	.photos {
		width: 100%;
		display: grid;
		grid-template-columns: repeat(5, 1fr);
		grid-gap: 8px;
	}
</style>
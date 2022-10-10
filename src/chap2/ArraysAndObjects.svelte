<script>
	let numbers = [1, 2, 3, 4];

	function addNumber() {
		numbers = [...numbers, numbers.length + 1]
	}

	$: sum = numbers.reduce((t, n) => t + n, 0);
</script>


<div class="root">
    <p>{numbers.join(' + ')} = {sum}</p>

    <button on:click={addNumber}>
        Add a number
    </button>
</div>

<style>
    .root {
        display: flex;
        justify-content: center;
    }
</style>

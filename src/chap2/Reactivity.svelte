<script>
	let count = 0;
	$: doubled = count * 2;
	$: if (count >= 10) {
		alert('count is dangerously high!');
		count = 9;
	}

	function handleClick() {
		count += 1;
	}
</script>

<div class="chap2-root">
    <button on:click={handleClick}>
        Clicked {count} {count === 1 ? 'time' : 'times'}
    </button>
    <p class="double-count">
        {count} doubeld is {doubled}
    </p>
</div>

<style>
    .chap2-root {
        display: flex;
        justify-content:center;
    }
    .double-count {
        margin-left: 24px;
    }
</style>
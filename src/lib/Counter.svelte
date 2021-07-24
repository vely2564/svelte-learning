<script>
	let count = 0; let doubled = 0;

	function incrementCount() {
    console.log('count');
		count += 1;
	}

  $: {
    console.log('doubled');
    doubled = count * 2;
  }
</script>

<button on:click={incrementCount}>
	Clicked {count} {count === 1 ? 'time' : 'times'}
</button>

<p>doubled is {doubled}</p>
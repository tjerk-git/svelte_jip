<h1>Hi</h1>

<script>
	import Robot from '../../components/robot.svelte';

	let count = 0;

	function handleClick() {
		count += 1;
	}
</script>

<Robot/>

<button on:click={handleClick}>
	Clicked {count} {count === 1 ? 'time' : 'times'}
</button>
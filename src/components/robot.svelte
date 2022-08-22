<script>
	import { cubicIn, quintOut } from 'svelte/easing';
	import { fade, draw, fly } from 'svelte/transition';
  import Roboto from '../components/Roboto.svelte';

	let visible = false;
  let dance = false;

  function handleShow() {
		visible = true;
	}

  function handleDance() {
    let dance = true;
	}
</script>

<div class="robot">
  {#if visible}
    <Roboto/>
  {/if}
</div>

<button on:click={handleShow}>
  Hi
</button>

<button on:click={handleDance}>
  Dance
</button>

<style>
  .robot{
    width:404px;
    height:431px;
  }
</style>
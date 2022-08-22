<script>
  export let open = false;
  import { slide } from 'svelte/transition';
	import { quintOut } from 'svelte/easing';
</script>


<button class:open on:click={() => open = !open}>
  Menu
</button>

{#if open}
<div class="container" transition:slide="{{delay: 250, duration: 300, easing: quintOut }}">
  <nav>
    <a href="/">Home</a>
    <a href="/about">About</a>
    <a href="/settings">Settings</a>
  </nav>
</div>
{/if}

<style>
  .container {
    width: 100vw;
    height: 100vh;
    background: black;
    margin: 0;
    position: absolute;
    z-index: 0;
  }

  button.open {
    color: white;
  }
  
  button {
    background: none;
    color: rgb(0, 0, 0);
    font-size: 22px;
    font-weight: bold;
    padding: 20px;
    width: 110px;
    position: absolute;
    top: 0;
    right: 0;
    border: none;
    cursor: pointer;
    z-index: 1;
    transition: background-color 400ms;
  }
</style>
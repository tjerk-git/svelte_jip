<script>
  let command = 'Command please...';
	import { cubicIn, quintOut } from 'svelte/easing';
	import { fade, draw, fly } from 'svelte/transition';
	let visible = true;
</script>


<div class="robot">
  {#if visible}
<svg width="204px" height="231px" viewBox="0 0 104 131" version="1.1" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink">
      <g id="Website_mobile" stroke="none" stroke-width="1" fill="none" fill-rule="evenodd">
          <g id="iPhone-13-mini" transform="translate(-136.000000, -163.000000)">
              <g id="Logo" transform="translate(136.000000, 163.000000)">
                  <rect in:draw="{{duration: 5000}}" id="Rectangle" stroke="#000000" stroke-width="3" fill="#FFFFFF" x="1.5" y="1.5" width="100.792308" height="100.792308" rx="2"></rect>
                  <rect in:draw="{{duration: 5000}}" id="Rectangle" stroke="#000000" stroke-width="3" fill="#FFFFFF" x="1.5" y="102.773077" width="100.792308" height="26.7269231"></rect>
                  <line in:draw="{{duration: 5000}}" x1="31.4903846" y1="115.128846" x2="73.8134615" y2="115.128846" id="Line" stroke="#000000" stroke-width="3" stroke-linecap="square"></line>
                  <circle in:fade="{{duration: 3000}}" id="Oval" fill="#000000" cx="92.7076923" cy="115.884615" r="2.01538462"></circle>
                  <text in:fly="{{duration: 400, delay: 5000}}" id="JIP" font-family="RobotoSlab-Light, Roboto Slab" font-size="50" font-weight="300" fill="#000000">
                      <tspan x="15" y="71">Hi!</tspan>
                  </text>
                  <circle id="Oval" fill="#000000" cx="12.0923077" cy="115.380769" r="2.01538462"></circle>
              </g>
          </g>
      </g>
  </svg>

  {/if}
</div>

<label>
	<input type="checkbox" bind:checked={visible}>
	toggle me
</label>

<input bind:value={command}>

<style>
  .robot{
    width:204px;
    height:231px;
  }
</style>
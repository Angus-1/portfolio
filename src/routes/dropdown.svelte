<script>
	import { slide } from "svelte/transition";
	export let entry
	let isOpen = false
	const toggle = () => isOpen = !isOpen
</script>

<button on:click={toggle} 
aria-expanded={isOpen}><svg style="tran" 
width="20"
height="40" 
fill="none" 
stroke-linecap="round" 
stroke-linejoin="round"
 stroke-width="2" 
 viewBox="0 0 24 24" 
 stroke="currentColor">
 <path d="M9 5l7 7-7 7"></path></svg> 
 {entry[0]} </button>
{#if isOpen}
<ul transition:slide={{ duration: 300 }}>
	{#each entry[1] as item}
	<li>	{item}	</li>
	{/each}
</ul>
{/if}

<style>
	button {
border: white;
background: none;
display:block; 
color: inherit; 
font-size: 36px; 
margin: 0; 
padding-bottom: 0.5em; 
padding-top: 0.5em;
position: center;
 }
 li {
border:1px solid #ffffff;
border-radius: 10px;
background:rgb(14, 45, 85);
display:block; 
color: inherit; 
font-size: 24px; 
margin: 0;
 }

    svg { 
		transition: transform 0.2s ease-in;
	}
	
	[aria-expanded=true] svg { transform: rotate(0.25turn); }
</style>

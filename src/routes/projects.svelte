<script>
	import Item from './dropdown.svelte'
	const data = {
		'Projects': 
      ["info here"],
      
		'Experience': ["exp here"],
		
	}
</script>
{#each Object.entries(data) as entry}
<Item {entry} />
{/each}
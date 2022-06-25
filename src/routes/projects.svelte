<script>
	import Item from './accordian.svelte'
	const data = {
		'Projects': 
      ["info here"],
      
		'Experience': ["info here"],
		
	}
</script>
{#each Object.entries(data) as entry}
<Item {entry} />
{/each}
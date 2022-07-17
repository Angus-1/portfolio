<script>
	const titles = [
		['Home', '#Home'],
		['About', '#About'],
		['Experience', '#Experience'],
		['Contact', '#Contact']
	];

	let innerWidth = 0
	let innerHeight = 0
	$: mobile = innerWidth < 1080;
</script>

<svelte:window bind:innerWidth bind:innerHeight />
<div class="nav-container">
	{#each titles as title}	
			<a class={!mobile ? "" : "mobile"} href={title[1]}>
				{title[0]}
        
			</a>
	{/each}
</div>

<div class="content">
  <slot></slot>
</div>

<style>
   :global(body) {
  background-color: #143957;
  color: #fffefe;
    background-image: url("./src/components/background3.jpg");     
    background-size: inherit;
    background-repeat: repeat;
}


  .nav-container {
        max-width: 100%;;
        margin: 3px auto;
        background-color: #143957;
        color:white;
        text-indent: 70px;
        border-radius: 15px;
        padding: 1rem;
        display: flex;
  }
  

  
  a:link {
color: white;
background-color: transparent;
text-decoration: none;
}

a:visited {
color: white;
background-color: transparent;
text-decoration: none;
}

a:hover {
color: rgba(126, 191, 245, 0.596);
background-color: transparent;
text-decoration: underline;
}

</style>
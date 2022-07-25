<script>
	const titles = [
		['Home', '#Home'],
		['About', '#About'],
		['Experience', '#Experience'],
		['Contact', '#Contact']
	];

  const foots = [
		['Made by Angel Santoyo', '#Home']
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
<!------------------ footer  below ------------------------>
<div class="footer">

  <div id="footerContent">
    {#each foots as foot}	
    <a class={!mobile ? "" : "mobile"} href={foot[1]}>
      {foot[0]}
    </a>
    {/each}
  </div>
</div>
<!------------------ css  below ------------------------>


<style global>
   :global(body) {
    height: 100%;
    background-color: #5db5fd;
    background-size: auto;
  color: #fffefe;
    background-image: ("./static/background2.jpg");     
    background-size: inherit;
    background-repeat: repeat;
   
}


  .nav-container {
        max-width: 100%;;
        margin: 3px auto;
        background-color: transparent;
        color:white;
        text-indent: 70px;
        border-radius: 10px;
        padding: 1rem;
        display: flex;
        font-weight: 600;
        font-size:x-large;
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

.footer{
    width:100%; 
    background-color: rgba(17, 17, 17, 0.993);
    border-radius: 5px;
}
.footerContent{
    margin: 0 auto; width: 960px;
    
}
 
</style>
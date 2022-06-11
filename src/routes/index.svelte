<!-- src/routes/index.svelte -->
<script>
	let src = './src/components/profile.png';
	let name = 'about me image';
</script>


<svelte:head>
 <title>Angel Santoyo</title>
</svelte:head>


<div class="container">
 <div class="info">
   <div class="animate-background">
     <div class="container info-container">
     <div class="info-text">
       <h1>
       <p class="animate-text-1">Angel Santoyo</p>
       <p class="animate-text-1">Major: Computer Science</p>
       <p class="text-2">California State University, Fullerton</p>
       <img {src} width="200px" alt="{name} image">

       </h1>
     </div>
     <h2 class="subtitle">
       
     </h2>
     <div style="color:black" class="scroll-button animate-scroll" tabindex="0">
       
     </div>
     </div>
   </div>
 </div>
</div>

<div class="background-div"></div>


  

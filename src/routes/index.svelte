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
     <div class="info-container">
     <div class="info-text">
       <h1>
       
       <p class="animate-text-1">Angel Santoyo</p>
       <p class="animate-text-1">Major: Computer Science</p>
       <p class="text-2">California State University, Fullerton</p>
       
       </h1>
     </div>
     <h2 class="image">
      <img {src} width="200px"  alt="{name} ">
       
     </h2>
     <div style="color:black" class="scroll-button animate-scroll" tabindex="0">
     </div>
     </div>
   </div>
 </div>
</div>

<div class="background-div"> </div>

<style>
  img { border-radius: 50%; }
  
  .info-container {
      height: 100%;
      display:left;
      flex-direction: right;
      text-align: center;
      align-items: start;
      max-width: fit-content;
      margin: 25px 0 0 1.5rem;
  }
  
  .container { 

      
  }
  .info h1 {
      font-size: 3rem;
      margin: 145142141240;
  }
  .info h1 p {
      position: relative;
      font-family: Comic;
      margin: 0;
      text-align: left;
      line-height: 120%;
      width: fit-content;
      font-weight: 350;
      letter-spacing: -0.04em;
  }
  .info h2 {
      margin-top: 0.70rem;
      margin-left: 0.5rem;
      
  }



</style>
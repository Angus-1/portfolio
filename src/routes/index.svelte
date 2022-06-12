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
        <img {src} width="155px"  alt="{name} ">
       <p class="animate-text-1">Angel Santoyo,</p>
       <p class="animate-text-1">Major: Computer Science</p>
       <p class="text-2">California State University, Fullerton</p>
       
       </h1>
     </div>
     <h2 class="subtitle">
      Hello!
     </h2>
    
     </div>
   </div>
 </div>
</div>
<div class="background-div"></div>

<style>
  img {
     border-radius: 45%;
     opacity: 1;
   }
  .info {
      text-align: center;
      position: relative;
  }       
  .info-container {
      height: 100%;
      display:flex;
      flex-direction: column;
      justify-content: center;
      text-align: left;
      align-items: start;
  }
  .container {
  max-width: 1000px;
      margin: 10px 0 0 -2.5rem;
  }
  .info h1 {
      font-size: 4rem;
      margin: 0;
  }
  .info h1 p {
      position: relative;
      font:  Comic;
      font-size:  50px;
      margin: 0;
  text-align: left;
      line-height: 130%;
      width: fit-content;
      font-weight: 500;
      letter-spacing: -0.03em;
  }

  .info h2 {
    
      max-width: 65ch;
      font-weight: 400;
      margin-top: 0.03rem;
  }
.background-div {
  width: 100%;
  margin: -100px auto;
}

  .info .info-text {
      position: relative;
  }

</style>
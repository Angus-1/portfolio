<!-- src/routes/index.svelte -->




<svelte:head>
 <title>Angel Santoyo</title>
</svelte:head>

<div class="container">
 
       <h1>
       <p class="text-1">Hello! My name is</p>
       <p class="text-2"> Angel</p>
       </h1>
       <p class="text-3"> Computer science student</p>
       <p class="subtitle"> California State University, Fullerton </p>
     </div>
     

<div class="background-div"></div>

<style>
  .container {
    position: relative;
      max-width: fit-content;
      text-align: left;
      font:  Comic;
      margin: 0rem 0rem 0rem -5rem;
      line-height: 4rem;
  }
  .text-1 {
      font-size: 4rem;
      margin: 0rem;
      font-weight: 200;
      letter-spacing: -0.03em;
  }
 .text-2{
  font-size: 4rem;
  margin: 0rem;
  font-weight: 500;
  
 }   
 .text-3{
  font-size: 3rem;  
  margin: 0rem;
  margin-top: 0rem;
  font-weight: 200;
  line-height: 3rem;
 }    

  .subtitle {
     font-size: 2rem;
     margin: 0rem;
    font-weight: 200;
  }

 
</style>
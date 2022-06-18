
<svelte:head>
   <title>About</title>
</svelte:head>
<div class="container">
   <section>
       <div class="inner-container">
         <h2 class="about-title">About me</h2>
         <div class = "header-image"></div>
         <div class="about-subtitle">
             <p>
            I'm a first generation student majoring in computer science at California State University, Fullerton. 
            I'm very passionate about learning new concepts regularly, specifically about web development, game development/design, as well as software engineering. Outside of school I like to play video games, learn about cars, and try new foods.
             </p>
             
         </div>
       </div>
     </section>
</div>

<style>
  .about-title {
       font-size: 3.0rem;
       font-weight: bold;
       margin-top: 2rem;
   }
   .about-subtitle {
       margin-top: -2rem;
   }
   .about-subtitle >p {
       width: 70%;
       font-weight: bold;
       font-size: 1.5rem;
       line-height: 2rem;
   }
</style>
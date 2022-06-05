<!-- src/routes/about.svelte -->
<svelte:head>
   <title>About</title>
</svelte:head>
<link rel="stylesheet" href="https://cdn.simplecss.org/simple.min.css" >
<div class="main_container">
   <section>
       <div class="inner-container">
         <h2 class="about-title">About me</h2>
         <div class="about-subtitle">
             <p>
            I'm a first generation student majoring in computer science at CSU Fullerton. 
            I'm very passionate about learning new concepts regularly, specifically about web development, game development and design, as well as software engineering. Outside of school I like to play video games, and  learn about/work on my car and friend's cars.
             </p>
             <p>
               Email: 
                <span class="info-text">santoyox714@gmail.com</span>
                <br>
               Github: 
                <span class="info-text">github.com/Angus-1</span>
             </p>
         </div>
       </div>
     </section>
</div>
<style>
   .main_container {
       margin: 0 80px 0 65px;
   }
   .about-title {
       font-size: 4.2rem;
       font-weight: bold;
       margin-top: 11rem;
   }
   .about-subtitle {
       margin-top: -2rem;
   }
   .about-subtitle >p {
       width: 60%;
       font-weight: normal;
       font-size: 1rem;
       line-height: 2rem;
   }
   .info-text {
       font-style: italic;
       font-weight: bold;
   }
</style>
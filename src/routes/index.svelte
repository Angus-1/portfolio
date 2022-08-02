<!-- src/routes/index.svelte -->

<script>
  import Dropdown from '../components/dropdown.svelte';
  import { projects } from '../components/projects';
import { experiences } from '../components/experience';
  let Github = './static/github.png';
	let Gmail = './static/gmail.png';
  let Linkedin = './static/linkedin';
  let name = 'contact image';


  
	let innerWidth = 0
	let innerHeight = 0
	$: mobile = innerWidth < 1080;
</script>

<svelte:window bind:innerWidth bind:innerHeight />
<svelte:head>
 <title>Angel Santoyo</title>
</svelte:head>

<!------------------ welcome below ------------------------>

<section id = welcome> 
<div class="welcome-container">
 
       <h1>
       <p class="text-1">Hello! My name is</p>
       <p class="text-2"> Angel</p> <br>
       </h1>
       <p class="text-3"> 💻 Aspiring Software Engineer 📱 </p> <br>
       <p class="subtitle">   🔹 California State University, Fullerton 🔸  </p>
     </div>
     

<div class="background-div"></div>
</section>

<!------------------ about below ------------------------>

<section id = About> 
<div class="about-container">
   <section>
         <h2 class="about-title">About me</h2><br><br>
         <div class = "header-image"></div>
         <div class="about-subtitle">
             <p>
            I'm a first generation student majoring in computer science at California State University, Fullerton. <br><br>
            
            I really enjoy learning new concepts on a regular basis, some fields I find pretty interesting to research in my free time are web development, game development, and occasionally cyber security. <br><br>
           
            Outside of school I like to play video games, learn about cars, lift weights, listen to many types of music genres, and try new foods. My favorite game franchise is the Elder Scrolls series and my favorite food is Sushi! 
             </p>     
       </div>
     </section>
</div>
</section>

<!------------------ work below ------------------------>
<section id="Experience">
  <div class="prof-exp"> 
	<div class="work-experience">
		<h1 class="exp-header">Experience  </h1>			
			{#each experiences as experience}
				<Dropdown heading={experience.heading} content={experience.content} link={experience.link}/>
			{/each}
		</div></div>

    <div class="projects">
      <h1 class="project-experience">Projects </h1>			
        {#each projects as project}
          <Dropdown heading={project.heading} content={project.content} link={project.link}/>
        {/each}
      </div>
</section>

		

  

   <!------------------ css below ------------------------> 
<style>
      /*------------------  welcome css  ------------------ */
      :global(body) {
  background-color: #143957;
  color: #fffefe;
  background-image: radial-gradient(circle,#069ac7, rgb(5, 58, 128),#111111);
    background-size: inherit;
    background-repeat: repeat;
    
}

  .welcome-container {
      position: relative;
      max-width: fit-content;
      text-align: left;
      font:  Comic;
      margin: 0rem 0rem 0rem -5rem;
      line-height: 4rem;
      margin: 0;
      top: 10rem;
      padding:0;
      
  }
  .text-1 {
      font-size: 4rem;
      margin: 0rem;
      font-weight: 200;
      letter-spacing: -0.03em;
      color:white;
      line-height: 1.0;
      max-width: 100%;
  }
 .text-2{
  font-size: 4rem;
  margin: 0rem;
  font-weight: 500;
  color:white;
  line-height: 1.5;
  
 }   
 .text-3{
  font-size: 3rem;  
  margin: 0rem;
  margin-top: 0rem;
  font-weight: 200;
  line-height: 3rem;
  color:white;
 }    
 
  .subtitle {
     font-size: 2.0rem;
     margin: 0rem;
    font-weight: 200;
    color:white;
    padding-left: 2vw;
    padding-right: 2vw;
  }

 /*------------------  about css  ------------------ */
  .about-container {
      position: relative;
      top: 12rem;
      padding:0;
      background-color: #053f6e; 
      background-position-x: right; 
      border-radius: 10px;
      padding-left: 20px;
      padding-bottom: 10px;
  }
  .about-title {
       font-size: 3.0rem;
       font-weight: 650;
       margin-top: 30rem;
       color:white;
       text-align: center;
   }
   
   .about-subtitle {
       margin-top: -2rem;
       width: 70%;
       font-weight: 500;
       font-size: 1.5rem;
       line-height: 2rem;
       color:white;
   }


 /*------------------  experience css  ------------------ */

   .prof-exp{
    margin-top: 40rem;
    margin-bottom: 10rem;
    position: relative;
    top: 7rem;
    color:white;
    background-color: #053f6e; 
    padding:0;
    border-radius: 10px;
    padding-left: 10px;
   }

   .projects{
    position: relative;
    color:white;
    background-color: #053f6e;  
    padding:0;
    border-radius: 10px;
    padding-left: 10px; 
    margin-bottom: 15rem;
    
   }




/*------------------  footer css  ------------------ */


</style>
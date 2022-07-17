<!-- src/routes/index.svelte -->

<script>
  import Dropdown from '../components/dropdown.svelte';
  import { projects } from '../components/projects';
import { experiences } from '../components/experience';
  
</script>


<svelte:head>
 <title>Angel Santoyo</title>
</svelte:head>

<!------------------ welcome below ------------------------>
<section id = welcome> 
<div class="container">
 
       <h1>
       <p class="text-1">Hello! My name is</p>
       <p class="text-2"> Angel</p>
       </h1>
       <p class="text-3"> Computer science student</p>
       <p class="subtitle"> California State University, Fullerton </p>
     </div>
     

<div class="background-div"></div>
</section>

<!------------------ about below ------------------------>

<section id = about> 
<div class="container">
   <section>
       
         <h2 class="about-title">About me</h2>
         <div class = "header-image"></div>
         <div class="about-subtitle">
             <p>
            I'm a first generation student majoring in computer science at California State University, Fullerton. 
            I'm very passionate about learning new concepts regularly, specifically about web development, game development/design, and software engineering. Outside of school I like to play video games, learn about cars, and try new foods.
             </p>
             
       </div>
     </section>
</div>
</section>

<!------------------ work below ------------------------>
<section id="experience">
  <div class="experience-space"> 
	<div class="work-experience">
		<h1 class="header">Experience</h1>			
			{#each experiences as experience}
				<Dropdown heading={experience.heading} content={experience.content} link={experience.link}/>
			{/each}
		</div>

    <div class="projects">
      <h1 class="project-experience">Projects</h1>			
        {#each projects as project}
          <Dropdown heading={project.heading} content={project.content} link={project.link}/>
        {/each}
      </div>
    </div>
</section>

		

<!------------------ contact below ------------------------>

    <section id="contact">   
      <div class="contact-info">
        <p>   
            <span class="contact-text"> 
            <a href="http://www.santoyox714@gmail.com"> Email: santoyox714@gmail.com </a>
            </span>
            <br>
            <span class="contact-text2">  
                <a href="https://github.com/Angus-1"> Github: github.com/Angus-1 </a>
            </span>
            <br>
             <span class="contact-text3">
                <a href="https://www.linkedin.com/in/asantoyo/"> Linkedin: linkedin.com/in/asantoyo/</a>
             </span>
         </p>
        </div>
  </section>

   <!------------------ css below ------------------------> 
<style>
   
  .container {
    position: relative;
      max-width: fit-content;
      text-align: left;
      font:  Comic;
      margin: 0rem 0rem 0rem -5rem;
      line-height: 4rem;
      margin: 0;
      padding:0;
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
  .about-title {
       font-size: 3.0rem;
       font-weight: 650;
       margin-top: 30rem;
   }
   
   .about-subtitle {
       margin-top: -2rem;
       width: 70%;
       font-weight: 500;
       font-size: 1.5rem;
       line-height: 2rem;
   }
   .experience-space{
    margin-top: 30rem;
   }

   .contact-info {
    margin-top: 20rem;
  width:500px;
  height:125px;
  border:1px solid #ffffff;
  background:rgb(38, 88, 153);;
  position:center;
  border-radius: 10px;
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
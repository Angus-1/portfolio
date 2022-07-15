<script>
    import Dropdown from '../components/dropdown.svelte';
    import { projects } from '../components/projects';
	import { experience } from '../components/experience';
    
</script>


<section id="experience">
	<div class="experience">
		<h1 class="header">Experience</h1>			
			{#each projects as project}
				<Dropdown heading={project.heading} content={project.content} link={project.link}/>
			{/each}
		</div>
</section>




<section id="projects">
			<div class="projects">
				<h1 class="header">Projects</h1>			
					{#each projects as project}
						<Dropdown heading={project.heading} content={project.content} link={project.link}/>
					{/each}
				</div>
		</section>

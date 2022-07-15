<script lang="ts">
	import { slide } from 'svelte/transition';
	export let heading: String;
	export let content: String;
	export let link: string;
	let isOpen = false;
	const toggle = () => (isOpen = !isOpen);
</script>

<div class="Dropdown">
	<button class={isOpen ? 'active' : ''} on:click={toggle} aria-expanded={isOpen}>
		<span class="heading">{heading}</span>
		{#if isOpen}
			<span class="icon">&minus;</span>
		{:else}
			<span class="icon">&plus;</span>
		{/if}
	</button>

	{#if isOpen}
		<span class="inside" transition:slide={{ duration: 300 }}>
			<p>
				{content}
			</p>
			<div class="link">
				<a href={link} class="link-text" target="_blank" rel="noopener noreferrer">
					Link
				</a>
			</div>
		</span>
	{/if}
</div>


<style>
	p {
		color: var(--left);
		padding: 0.3rem 1.5rem;
	}

	button {
		 
		border: white;
		background: none;
		display:block; 
		color: inherit; 
		cursor: pointer;
		font-size: 1.75rem; 
		margin: 0;
		padding-bottom: 0.5em; 
		padding-top: 0.5em;
		position: center;
		border-radius: 25px;
		justify-content: space-between;
		align-items: center;
		
		
		display: flex;
		color: var(--left);
		
		
	
		padding: 0.5em;
	}

	button:hover {
		border-radius: 25px;
		background-color: rgb(57, 105, 168);
		color: var(--text);
	}

	button:active {
		border-radius: 25px;
		background-color: var(--split);
		color: var(--text);
	}

	a:link {
		
		text-decoration: none;
		color: var(--left);
	}

	a:visited {
		
		text-decoration: none;
		color: var(--left);
	}

	.inside {
		border-radius: 25px;
		background-color: rgb(57, 105, 168);
		text-align: left;
		height: auto;
		margin: 0;
		padding-right: 0;
	}

	.active {
		
		background-color: var(--split);
		color: var(--text);
	}
	.Dropdown {
		border-radius: 25px;
		display: flex;
		flex-direction: column;
		width: 100%;
	}

	.Dropdown .inside {
		width: 100%;
	}

	.Dropdown button {
		width: 100%;
	}

	.link {
		border-radius: 25px;
		background-color: var(--text);
		display: flex;
		align-items: center;
		justify-content: center;
		color: rgb(62, 104, 241);
		font-size: 1.5rem;
		margin: 0;
		padding: 0.5em;
	}

	.link-text {
		color: var(--left);
		border: 2px solid var(--left);
		
	}

	.link-text:hover {
		background-color: var(--left);
		color: var(--text);
	}
</style>
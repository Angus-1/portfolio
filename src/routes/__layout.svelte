<!-- src/routes/__layout.svelte -->
<nav>
    <div class="nav-container">
        <a href="/" class="nav-logo" title="Back to Homepage">Home</a>
        <div class="nav-links">
            <a href="/about" class="link">About</a>
            <a href="/projects" class="link">Projects</a>
            <a href="/contact" class="link">Contact</a>
        </div>
    </div>
 </nav>
 
 <div class="container">
  <!-- Pages will be injected below -->
     <slot></slot>
 </div>
 
 <style>
    .container {
        max-width: 1400px;
        margin: 50px auto;
    }
    :global(body) {
		background-color: #1d3040;
		color: #bfc2c7;
	}


 </style>
     
    
<!-- src/routes/__layout.svelte -->
<nav>
    <div class="nav-container">
        <a href="/" class="nav-logo" title="Back to Homepage">Home</a>
       
            <a href="/about" class="link">About</a>
            <a href="/projects" class="link">Projects</a>
            <a href="/contact" class="link">Contact</a>
            <div class="nav-links">
        </div>
    </div>
 </nav>
 
 <div class="container">
 
     <slot></slot>
 </div>
 
 <style>
     :global(body) {
		background-color: #143957;
		color: #ffffff;
        background-image: url("./src/components/background2.jpg");     
	}
    .nav-container {
        max-width: 1000px;
        margin: 2px auto;
        background-color: #143957;
        color:white
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
     
    
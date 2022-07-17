<!-- src/routes/__layout.svelte -->
<nav>
    <div class="nav-container">
        <a href="/" class="nav-logo" title="Back to Homepage">Home</a>
        <meta name="viewport" content="width=device-width, initial-scale=1.0">

            <a href="/#About" class="link">About  </a>
            <a href="/#Experience" class="link">Experience  </a>
            <a href="/#Contact" class="link">Contact  </a>
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
		color: #fffefe;
      background-image: url("./static/background2.jpg");     
      background-size: 100%;
      background-repeat: repeat;
	}
  
  .container {
       max-width: 1400px;
       margin: 50px auto;
   }
    .nav-container {
        max-width: 100%;;
        margin: 2px auto;
        background-color: #143957;
        color:white;
        text-indent: 50px;
        border-radius: 15px;
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
     
    
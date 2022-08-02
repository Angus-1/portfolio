<script>
	const titles = [
		['Home', '#Home'],
		['About', '#About'],
		['Experience', '#Experience']
	];

  const foots = [
		['Made by Angel Santoyo', '#Home']
	];

	let innerWidth = 0
	let innerHeight = 0
	$: mobile = innerWidth < 1080;

</script>

<svelte:window bind:innerWidth bind:innerHeight />
<div class="nav-container">
	{#each titles as title}	
			<a class={!mobile ? "" : "mobile"} href={title[1]}>
				{title[0]}
        
			</a>
	{/each}
</div>

<div class="content">
  <slot></slot>
</div>
<!------------------ footer  below ------------------------>

  <footer>
      <div class="footer-content">
          <h3>Angel Santoyo</h3>
          <p>Feel free to contact me below</p>
         

          <ul class="socials">
            <section id="Contact">   
              <div class="contact-info">
                <p>   
                        <a href="mailto:santoyox714@gmail.com">         <img src = 'gmail.png'   width="65px"  alt=git/> </a>            
                        <a href="https://github.com/Angus-1">            <img src = 'github.png'  width="65px" alt=gmail/> </a>          
                        <a href="https://www.linkedin.com/in/asantoyo/"> <img src = 'linkedin.png'width="60px" alt=linkedin/> </a>

                </div>
          </section>
          </ul>
      </div>
      <div class="footer-bottom">
          <p>copyright &copy; <a href="#">2022</a>  </p>
                  <div class="footer-menu">
                    <ul class="f-menu">
                      <li><a href="#">Home</a></li>
                      <li><a href="#About">About</a></li>
                      <li><a href="#Experience">Experience</a></li>
                      
                    </ul>
                  </div>
      </div>

  </footer>

<!------------------ css  below ------------------------>


<style global>
   :global(body) {
    height: 100%;
    background-color: #5db5fd;
    background-size: auto;
  color: #fffefe;
    background-image: ("./static/background6.jpg");     
    background-size: inherit;
    background-repeat: repeat;
   
}


  .nav-container {
        max-width: 100%;;
        margin: 3px auto;
        background-color: transparent;
        border-radius: 10px;
        padding: 1rem;
        display: flex;
        font-weight: 600;
        font-size:x-large;
        padding: 2rem;
		    padding-left: 5vw;
		    padding-right: 5vw;
		    justify-content: space-evenly;
		    align-items: center;
		    width: auto;
		    list-style: none;
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
 /*------------------  footer css  ------------------ */
*{
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}
body{
    background: #fcfcfc;
    font-family: sans-serif;
}
footer{
    position: absolute;
    bottom: 1;
    left: 0;
    right: 0;
    background: #111;
    height: auto;
    width: 100%;
    padding-top: 40px;
    color: #fff;
}
.footer-content{
    display: flex;
    align-items: center;
    justify-content: center;
    flex-direction: column;
    text-align: center;
}
.footer-content h3{
    font-size: 2.1rem;
    font-weight: 500;
    text-transform: capitalize;
    line-height: 3rem;
}
.footer-content p{
    max-width: 500px;
    margin: 10px auto;
    
   
    color: #cacdd2;
    
} 
.contact-info {
  height:125px;
  background-color:transparent ;
  font-weight: 600;
  font-size: large;
  line-height: 2;
}

.socials{
    list-style: none;
    display: flex;
    align-items: center;
    justify-content: center;
    margin: 1rem 0 3rem 0;
    
}
.socials li{
    margin: 0 10px;
}
.socials a{
    text-decoration: none;
    color: #fff;
    border: transparent;
    padding: 5px;

    border-radius: 50%;

}
.socials a i{
    font-size: 1.1rem;
    width: 20px;
    transition: color .4s ease;

}
.socials a:hover i{
    color: aqua;
}

.footer-bottom{
    background: #000;
    width: 100vw;
    padding: 20px;
padding-bottom: 40px;
    text-align: center;
}
.footer-bottom p{
float: left;
    font-size: 14px;
    word-spacing: 2px;
    text-transform: capitalize;
}
.footer-bottom p a{
  color:#44bae8;
  font-size: 16px;
  text-decoration: none;
}
.footer-bottom span{
    text-transform: uppercase;
    opacity: .4;
    font-weight: 200;
}
.footer-menu{
  float: right;

}
.footer-menu ul{
  display: flex;
}
.footer-menu ul li{
padding-right: 10px;
display: block;
}
.footer-menu ul li a{
  color: #cfd2d6;
  text-decoration: none;
}
.footer-menu ul li a:hover{
  color: #27bcda;
}

@media (max-width:500px) {
.footer-menu ul{
  display: flex;
  margin-top: 10px;
  margin-bottom: 20px;
}
}
 
</style>
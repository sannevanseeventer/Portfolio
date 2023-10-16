<script>
     import { gsap } from "gsap";
    import { ScrollTrigger } from "gsap/dist/ScrollTrigger";
    import { onMount } from "svelte";
    
    onMount(() => {
const details = gsap.utils.toArray(".desktopContentSection:not(:first-child)")
const photos = gsap.utils.toArray(".desktopPhoto:not(:first-child)")


gsap.set(photos, {yPercent:101})

const allPhotos = gsap.utils.toArray(".desktopPhoto")


// create
let mm = gsap.matchMedia();

// add a media query. When it matches, the associated function will run
mm.add("(min-width: 600px)", () => {

  // this setup code only runs when viewport is at least 600px wide
  console.log("desktop")
	
  ScrollTrigger.create({
	trigger:".gallery",
	start:"top top",
	end:"bottom bottom",
	pin:".right"
})

//create scrolltrigger for each details section
//trigger photo animation when headline of each details section 
//reaches 80% of window height
details.forEach((detail, index)=> {

	let headline = detail.querySelector("h1")
	let animation = gsap.timeline()
	   .to(photos[index], {yPercent:0})
	   .set(allPhotos[index], {autoAlpha:0})
	ScrollTrigger.create({
		trigger:headline,
		start:"top 80%",
		end:"top 50%",
		animation:animation,
		scrub:true,
		markers:false
	})
})
	
	
  
  return () => { // optional
    // custom cleanup code here (runs when it STOPS matching)
	  console.log("mobile")
  };
});
});
</script>

<section>
  <!-- <div class="spacer"></div> -->

<div class="gallery">
	<div class="left">
		<div class="desktopContent">
			<div class="desktopContentSection">
				<h1>The Ocean Cleanup</h1>
				<p>Voor GRRR, een digital agency in Amsterdam, heb ik een concept mogen ontwerpen voor The Ocean Cleanup. De bedoeling was om data van de verschillende Interceptors en hoeveelheid opgeruimd plastic zo overzichtelijk mogelijk weer te geven.</p>
			  <li><a href="www.google.com">Bekijk project</a></li>
      </div>
			<div class="desktopContentSection">
        <h1>SPATwater</h1>
				<p>Voor GRRR, een digital agency in Amsterdam, heb ik een concept mogen ontwerpen voor The Ocean Cleanup. De bedoeling was om data van de verschillende Interceptors en hoeveelheid opgeruimd plastic zo overzichtelijk mogelijk weer te geven.</p>
			  <li><a href="www.google.com">Bekijk project</a></li>
      </div>
			<div class="desktopContentSection">
        <h1>UltiTV</h1>
				<p>Voor GRRR, een digital agency in Amsterdam, heb ik een concept mogen ontwerpen voor The Ocean Cleanup. De bedoeling was om data van de verschillende Interceptors en hoeveelheid opgeruimd plastic zo overzichtelijk mogelijk weer te geven.</p>
			  <li><a href="www.google.com">Bekijk project</a></li>
     
      </div>
			<div class="desktopContentSection">
        <h1>Squad page FDND jaar 2</h1>
				<p>Voor GRRR, een digital agency in Amsterdam, heb ik een concept mogen ontwerpen voor The Ocean Cleanup. De bedoeling was om data van de verschillende Interceptors en hoeveelheid opgeruimd plastic zo overzichtelijk mogelijk weer te geven.</p>
			  <li><a href="www.google.com">Bekijk project</a></li>
      </div>

      <div class="desktopContentSection">
        <h1>Squad page FDND jaar 1</h1>
				<p>Voor GRRR, een digital agency in Amsterdam, heb ik een concept mogen ontwerpen voor The Ocean Cleanup. De bedoeling was om data van de verschillende Interceptors en hoeveelheid opgeruimd plastic zo overzichtelijk mogelijk weer te geven.</p>
			  <li><a href="www.google.com">Bekijk project</a></li>
      </div>

		</div>
	</div>

	<div class="right">

    <div class="desktopPhotos">
			<div class="desktopPhoto red"></div>
			<div class="desktopPhoto green"></div>
      <div class="desktopPhoto blue"></div>
			<div class="desktopPhoto pink"></div>
      <div class="desktopPhoto yellow"></div>
		</div>

	</div>
</div>

<!-- <div class="spacer"></div>
<div class="spacer"></div>
<div class="spacer"></div> -->
  <!-- <div class="line" /> -->
<!-- 
  <div class="marquee">
    <div class="marquee-content scroll">
      <div>Projecten -</div>
      <div>Projecten -</div>
      <div>Projecten -</div>
      <div>Projecten -</div>
    </div>
    <div class="marquee-content scroll">
      <div>Projecten -</div>
      <div>Projecten -</div>
      <div>Projecten -</div>
      <div>Projecten -</div>
    </div>
  </div> -->

  <!-- <h1>Projecten</h1> -->

  <!-- GOOOOD SECTION -->
  <div class="project-container">
    <div class="project-1">
      <a href="/OceanCleanup"><img src="/oceancleanup.png" alt="foto van project OceanCleanup" /></a>

      <div class="content-container">
      <h2>The Ocean Cleanup</h2>
      <i class="ri-arrow-right-circle-fill"></i>
        
    </div>
    <div class="line"></div>
    </div>

    <div class="project-3">
      <img src="/spatwater.png" alt="foto van project Spatwater" />
      <div class="content-container">
      <h2>SPATwater</h2>
      <i class="ri-arrow-right-circle-fill"></i>
        
      </div>
      <div class="line"></div>
    </div>



    <div class="project-4">
      <img src="/ultitv2.png" alt="foto van project OceanCleanup" />
      <div class="content-container">
      <h2>UltiTV</h2>
      <i class="ri-arrow-right-circle-fill"></i>
      </div>
      <div class="line"></div>
    </div>



    <div class="project-4">
      <img src="/bookshelf.png" alt="foto van project OceanCleanup" />
      <div class="content-container">
      <h2>Squad page FDND jaar 2</h2>
      <i class="ri-arrow-right-circle-fill"></i>
      </div>
      <div class="line"></div>
    </div>


    <div class="project-2">
      <img src="/squadpage4.png" alt="foto van project OceanCleanup" />
      <div class="content-container">
      <h2>Squad page FDND jaar 1</h2>
      <i class="ri-arrow-right-circle-fill"></i>
      </div>
      <div class="line"></div>
    </div>


  </div>
  <!-- GOOOOOD SECTION END -->
</section>

<style>
  /* END TEST */

  section {
    width: 100vw;
    height: auto;
    padding-bottom: 4rem;
    /* background-color: white; */
  }

  .gallery{
    display: none;
  }

  .line {
    border-bottom: 1px solid #e7e7e7;
    margin-top: 0.3rem;
  }

  /* h1{
    font-size: 1.1rem;
    color: #1273ea;
    font-family: "Poppins";
    font-weight: 400;
    padding-left: 1rem;
    margin-bottom: 1rem;
  } */
 
/* 
  .marquee {
    display: flex;
    overflow: hidden;
    padding: 2rem;
    gap: 1rem;
    z-index: -1;
  }
  .marquee-content {
    flex-shrink: 0;
    display: flex;
    justify-content: space-around;
    min-width: 100%;
    gap: 1rem;
    font-family: "Helvetica";
    font-size: 2.5rem;
    text-transform: uppercase;
  }

  @keyframes scroll {
    from {
      transform: translateX(0);
    }
    to {
      transform: translateX(calc(-100% - 1rem));
    }
  }
  .scroll {
    animation: scroll 30s linear infinite;
  } */

  h2 {
    font-family: "Poppins";
    font-size: .9rem;
    font-weight: 400;
  }
  .project-container {
    width: 90vw;
    margin: 0 auto;
    display: flex;
    flex-direction: column;
    gap: 4rem;
  }

  .project-container img {
    width: 100%;
    z-index: 1;
  }

  .content-container{
    display: flex;
    justify-content: space-between;
    align-items: center;

  }

  i{
    color:  #1273ea;
font-size: 1.6rem;
  }

  @media only screen and (min-width: 1024px) {
/* TEST */

.project-container{
  display: none;
}


.gallery h1 {
	font-size:clamp(1em, 4vw, 2.5em);
  margin-bottom: 1rem;
}

.gallery p {
	font-size:clamp(1.4em, 2.5vw, .9em);
  font-family: "poppins";
	line-height:1.4;
  margin-bottom: 1.5rem;
}


.gallery {
  display:flex;	
  margin-top: 4rem;
  /* outline:1px solid red; */
}

.left {
	width:50%;
}

.right {
	height:100vh;
	/* outline:1px solid purple; */
	width:50%;
	display:flex;
	flex-direction:column;
	justify-content:center;
}

.desktopContent {
	margin:auto;
	width:80%;
}

.desktopContentSection {
	min-height:100vh;
	/* outline:1px solid green; */
	display:flex;
	flex-direction:column;
	justify-content:center;
}


.desktopPhotos {
	width:40vw;
	height:35vw;
	position:relative;
	overflow:hidden;
}

.desktopPhoto {
	position:absolute;
	width:100%;
	height:100%;
}

.red {
	background: crimson;
  background-image: url("/oceancleanup.png");
  background-size: cover;
  background-position: center;
  background-repeat: no-repeat;
}

.green {
	background:MediumSeaGreen;
  background-image: url("/spatwater2.png");
  background-size: cover;
  background-position: center;
  background-repeat: no-repeat;
}

.blue {
	background:dodgerblue;
  background-image: url("/ultitv2.png");
  background-size: cover;
  background-position: center;
  background-repeat: no-repeat;

}

.pink{
	background:deepPink;
  background-image: url("/bookshelf.png");
  background-size: cover;
  background-position: center;
  background-repeat: no-repeat;
}

.yellow{
	background:deepPink;
  background-image: url("/squadpage3.png");
  background-size: cover;
  background-position: center;
  background-repeat: no-repeat;
}

li{
  list-style-type: none;
}
a{
    text-decoration: none;
    padding: .5rem 1rem;
    background-color: #1b82ff;
    color: white;
    font-family: "Poppins";
    cursor: pointer;
    text-transform: uppercase;
    font-size: 1rem;
    letter-spacing: .03rem;
  }

  }

</style>

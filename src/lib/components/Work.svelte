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

<section id="projects">
  <!-- <div class="spacer"></div> -->

<div class="gallery">
	<div class="left">
		<div class="desktopContent">

			<div class="desktopContentSection">
				<h1>The Ocean Cleanup</h1>
				<p>Voor GRRR, een digital agency in Amsterdam, heb ik een concept mogen ontwerpen voor The Ocean Cleanup. De bedoeling was om data van de verschillende Interceptors en hoeveelheid opgeruimd plastic zo overzichtelijk mogelijk weer te geven.</p>
			  <a href="https://repulsive-undershirt-duck.cyclic.app/">Bekijk project</a>
      </div>

			<div class="desktopContentSection">
        <h1>SPATwater</h1>
				<p>Voor een startup genaamd SPATwater heb ik een website mogen bouwen met een speels en creatieve uitstraling. Er zit een parallax in verwerkt en de illustraties heb ik zelf gemaakt. </p>
			  <a href="https://spatwater.netlify.app/">Bekijk project</a>
      </div>

			<div class="desktopContentSection">
        <h1>UltiTV</h1>
				<p>Voor UltiTV heb ik meegewerkt aan een redesign voor het commentators dashboard, om tijdens wedstrijden de score bij te houden en zichzelf in te lezen over de informatie van de spelers. </p>
			  <a href="https://rich-gray-barnacle-slip.cyclic.app/">Bekijk project</a>
     
      </div>
			<div class="desktopContentSection">
        <h1>Squad page FDND jaar 2</h1>
				<p>In mijn tweede studiejaar kreeg ik de opdracht om een  overzichtspagina te ontwerpen met alle online visitekaartjes op basis van een headless CMS en framework. Het idee is een boekenkast met in de boeken de studenten van dat jaar.  </p>
			  <a href="https://fdnd-yearbooks.netlify.app/">Bekijk project</a>
      </div>

      <div class="desktopContentSection">
        <h1>Squad page FDND jaar 1</h1>
				<p>In mijn eerste studiejaar kreeg ik de opdracht om in een team een overzichtspagina te ontwerpen met alle online visitekaartjes van mijn mede studenten. </p>
			  <a href="https://long-slug-loafers.cyclic.app/">Bekijk project</a>
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
     <img src="/oceancleanup.png" alt="foto van project OceanCleanup" />

      <div class="content-container">
      <h2>Ocean Cleanup</h2>
      <a href="/OceanCleanup"><i class="ri-arrow-right-circle-fill"></i></a>
        
    </div>
    <div class="line"></div>
    </div>

    <div class="project-3">
      <img src="/spatwater.png" alt="foto van project Spatwater" />
      <div class="content-container">
      <h2>SPATwater</h2>
      <a href="/SpatWater"><i class="ri-arrow-right-circle-fill"></i></a>
        
      </div>
      <div class="line"></div>
    </div>



    <div class="project-4">
      <img src="/ultitv2.png" alt="foto van project OceanCleanup" />
      <div class="content-container">
      <h2>UltiTV</h2>
      <a href="/UltiTv"><i class="ri-arrow-right-circle-fill"></i></a>
      </div>
      <div class="line"></div>
    </div>



    <div class="project-4">
      <img src="/bookshelf.png" alt="foto van project OceanCleanup" />
      <div class="content-container">
      <h2>Squad page FDND jaar 2</h2>
      <a href="/Squad2"><i class="ri-arrow-right-circle-fill"></i></a>
      </div>
      <div class="line"></div>
    </div>


    <div class="project-2">
      <img src="/squadpage3.png" alt="foto van project OceanCleanup" />
      <div class="content-container">
      <h2>Squad page FDND jaar 1</h2>
      <a href="/Squad1"><i class="ri-arrow-right-circle-fill"></i></a>
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
    margin-top: .5rem;
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
    margin-top: .5rem;

  }

  a{
    text-decoration: none;
  }

  i{
    color:  #1273ea;
font-size: 1.6rem;
cursor: pointer;
  }

  @media only screen and (min-width: 1024px) {
/* TEST */

.project-container{
  display: none;
}


.gallery h1 {
	font-size:clamp(1em, 4vw, 2.5em);
  margin-bottom: 1rem;
  font-family: "poppins";
  font-weight: 500;
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
  margin: auto;
	width:75%;
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
	height:30vw;
	position:relative;
	overflow:hidden;
  margin: auto;
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

a{
  max-width: 9.5rem;
    text-decoration: none;
    padding: .5rem 1rem;
    background-color: #1273ea;
    color: white;
    font-family: "Poppins";
    cursor: pointer;
    font-size: 1rem;
    letter-spacing: .03rem;
  }

  }

</style>

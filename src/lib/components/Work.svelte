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

	let headline = detail.querySelector("h2")
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

<div class="gallery">
	<div class="left">
		<div class="desktopContent">


      <div class="desktopContentSection">
        <h2>Online CV</h2>
				<p>Voor mijn eindproject heb ik een online CV gebouwd waar je doorheen kan scrollen. Op deze website staat informatie over mij, mijn portfolio, ervaring en meer. Alle illustraties heb ik zelf geïllustreerd in Affinity Designer. </p>
			  <a href="https://sannevanseeventer.nl/" target="_blank">Bekijk website</a>
      </div>

			<div class="desktopContentSection">
				<h2>Ocean Cleanup</h2>
				<p>Voor GRRR, een digital agency in Amsterdam, heb ik een concept mogen ontwerpen voor Ocean Cleanup. De bedoeling was om data van de verschillende Interceptors en hoeveelheid opgeruimd plastic zo overzichtelijk mogelijk weer te geven.</p>
      </div>

			<div class="desktopContentSection">
        <h2>SPATwater</h2>
				<p>Voor een startup genaamd SPATwater heb ik een website mogen bouwen met een speels en creatieve uitstraling. Er zit een parallax in verwerkt en de illustraties heb ik zelf gemaakt. Ik heb gebruik gemaakt van Sveltekit en een headless CMS.</p>
			  <a href="https://spatwater.nl/" target="_blank">Bekijk website</a>
      </div>

			<div class="desktopContentSection">
        <h2>UltiTV</h2>
				<p>Voor UltiTV heb ik meegewerkt aan een redesign voor het commentators dashboard voor Ultimate Frisbee. Met dit dashboard kan je tijdens wedstrijden de score bij houden en kunnen de wedstrijd commentatoren zichzelf inlezen over de informatie van de spelers. </p>
     
      </div>
			<div class="desktopContentSection">
        <h2>Boekenkast</h2>
				<p>In mijn tweede studiejaar kreeg ik de opdracht om een overzichtspagina te ontwerpen met online visitekaartjes op basis van een headless CMS en framework. Het idee is een boekenkast met in de boeken de studenten van dat jaar.  </p>
      </div>


		</div>
	</div>

	<div class="right">

    <div class="desktopPhotos">
      <div class="desktopPhoto yellow"></div>
			<div class="desktopPhoto red"></div>
			<div class="desktopPhoto green"></div>
      <div class="desktopPhoto blue"></div>
			<div class="desktopPhoto pink"></div>

		</div>

	</div>
</div>

  <!-- GOOOOD SECTION -->
  <div class="project-container">
    <div class="project-2">
      <img src="/cv-2.webp" alt="mockup van online cv" />
      <div class="content-container">
      <h2>Online CV</h2>
      <a href="/CV"><i class="ri-arrow-right-circle-fill"></i></a>
      </div>
      <div class="line"></div>
    </div>

    <div class="project-1">
     <img src="/oceancleanup.webp" alt="foto van project OceanCleanup" />

      <div class="content-container">
      <h2>Ocean Cleanup</h2>
      <a href="/OceanCleanup"><i class="ri-arrow-right-circle-fill"></i></a>
        
    </div>
    <div class="line"></div>
    </div>

    <div class="project-3">
      <img src="/spatwater.webp" alt="foto van project Spatwater" />
      <div class="content-container">
      <h2>SPATwater</h2>
      <a href="/SpatWater"><i class="ri-arrow-right-circle-fill"></i></a>
        
      </div>
      <div class="line"></div>
    </div>



    <div class="project-4">
      <img src="/ultitv2.webp" alt="foto van project OceanCleanup" />
      <div class="content-container">
      <h2>UltiTV</h2>
      <a href="/UltiTv"><i class="ri-arrow-right-circle-fill"></i></a>
      </div>
      <div class="line"></div>
    </div>



    <div class="project-4">
      <img src="/bookshelf.webp" alt="foto van project OceanCleanup" />
      <div class="content-container">
      <h2>Boekenkast</h2>
      <a href="/Squad2"><i class="ri-arrow-right-circle-fill"></i></a>
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


  h2 {
    font-family: "Poppins", sans-serif;
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
font-size: 2rem;
cursor: pointer;
  }

  @media only screen and (min-width: 1024px) {

.project-container{
  display: none;
}


.gallery h2 {
	font-size:clamp(1em, 4vw, 2.2em);
  margin-bottom: 1rem;
  font-family: "poppins", sans-serif;
  font-weight: 500;
}

.gallery p {
	font-size:clamp(1.4em, 2.5vw, .9em);
  font-family: "poppins", sans-serif;
	line-height:1.4;
  max-width: 42rem;
  margin-bottom: 2rem;
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
  background-image: url("/oceancleanup.webp");
  background-size: cover;
  background-position: center;
  background-repeat: no-repeat;
}

.green {
  background-image: url("/spatwater2.webp");
  background-size: cover;
  background-position: center;
  background-repeat: no-repeat;
}

.blue {
  background-image: url("/ultitv2.webp");
  background-size: cover;
  background-position: center;
  background-repeat: no-repeat;

}

.pink{
  background-image: url("/bookshelf.webp");
  background-size: cover;
  background-position: center;
  background-repeat: no-repeat;
}

.yellow{
  background-image: url("/cv-2.webp");
  background-size: cover;
  background-position: center;
  background-repeat: no-repeat;
}

a{
  max-width: 9.5rem;
    text-decoration: none;
    padding: .7rem 1rem;
    background-color: #1273ea;
    color: white;
    font-family: "Poppins", sans-serif;
    cursor: pointer;
    font-size: 1rem;
    letter-spacing: .03rem;
  }

  }

</style>

<script>
    import { gsap } from "gsap";
    import { ScrollTrigger } from "gsap/dist/ScrollTrigger";
    import { onMount } from "svelte";
    
  
    gsap.registerPlugin(ScrollTrigger);
  
    onMount(() => {
        const races = document.querySelector(".races");
console.log(races.offsetWidth)

function getScrollAmount() {
	let racesWidth = races.scrollWidth;
	return -(racesWidth - window.innerWidth);
}

const tween = gsap.to(races, {
	x: getScrollAmount,
	duration: 3,
	ease: "none",
});


ScrollTrigger.create({
	trigger:".racesWrapper",
	start:"top 30%",
	end: () => `+=${getScrollAmount() * -1}`,
	pin:true,
	animation:tween,
	scrub:2,
	invalidateOnRefresh:true,
	markers:false
})
    });
  </script>
  
  
<div class="space-50vh lightBG"></div>

<div class="racesWrapper">

    <div class="races2">
		<p>Grafisch vormgever en creatief frontend developer in spé based in Amsterdam. Mijn passie ligt bij design, layout, illustration & motion design.  </p>
	</div>

	<div class="races">
		<h2>Sanne</h2>
		<h2>van</h2>
		<h2>Seeventer</h2>
	</div>


</div>

<div class="space-10vh lightBG"></div>




  <style>
@import url("https://fonts.googleapis.com/css2?family=Alice&family=Kenia&family=Poppins:ital,wght@0,700;1,700&family=Righteous&family=Roboto:ital,wght@0,100;0,300;0,400;0,700;1,300&display=swap");
@import url('https://fonts.googleapis.com/css2?family=Bebas+Neue&family=Open+Sans:wght@400;500;600&family=Poppins:wght@400;500;600&display=swap');

.races {
	width:fit-content;
	display:flex;
	flex-wrap:nowrap;
}

p{
    font-size: .9rem;
    color: rgb(0, 0, 0);
    text-align: left;
    margin: auto;
    font-family: "Poppins";
    padding: 1rem 1rem 1rem 1rem;
}

.races h2 {
	font-family: 'Bebas Neue';
	font-size:35vw;
    font-weight: 500;
	flex-shrink:0;
	padding-right:0.3em;
    padding-left: 0.5rem;
    letter-spacing: .2rem;
	color:black;
	margin:0;	
}

.races h2:last-of-type {
	background: #1273ea;
    color: white;
}

.lightBG {
	background: white;
}

.space-10vh {
	height:10vh;
}

.space-50vh {
	height:60vh;
}

@media only screen and (min-width: 1024px) {

.races h2 {
	font-size:26.5vw;
	margin-left: 2rem;
}

.races h2:last-of-type {
	padding-left: 5rem;

}

.space-50vh {
	height:25vh;
}

p{
    font-size: 1.5rem;
	margin: 3rem 0rem 1rem 2.5rem;
	max-width: 35rem;
}

}
  </style>
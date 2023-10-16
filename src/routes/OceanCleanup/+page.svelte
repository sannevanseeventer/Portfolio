<script>
  import Nav2 from "$lib/components/Nav2.svelte";
</script>

<Nav2 />

<section>

  <div class="project1-container">

    <h2>Ocean Cleanup</h2>

<p>Voor GRRR, een digital agency in Amsterdam, heb ik een concept mogen ontwerpen voor Ocean Cleanup. De bedoeling was om data van de verschillende Interceptors en hoeveelheid opgeruimd plastic zo overzichtelijk mogelijk weer te geven.</p>

<ul>
  <li><a href="https://repulsive-undershirt-duck.cyclic.app/">Bekijk project</a></li>
</ul>


<img src="/oceancleanup.png" alt="foto van project OceanCleanup" />
<img src="/oceancleanup2.png" alt="foto van project OceanCleanup" />


</div>
</section>

<style>
  	@import url("https://fonts.googleapis.com/css2?family=Alice&family=Kenia&family=Poppins:ital,wght@0,700;1,700&family=Righteous&family=Roboto:ital,wght@0,100;0,300;0,400;0,700;1,300&display=swap");
	@import url('https://fonts.googleapis.com/css2?family=Bebas+Neue&family=Open+Sans:wght@400;500;600&family=Poppins:wght@400;500;600&display=swap');

  section{
   width: 100vw;
    height: auto;
    padding: 1rem;
    background-color: white;
  }

  .project1-container{
    margin-top: 5rem;
  }

  h2{
    font-size: 1.2rem;
    margin-bottom: 1rem;
    font-family: "poppins";
    font-weight: 500;
  }

  p{
    margin-bottom: 1rem;
    font-size: 0.9rem;
    font-family: "poppins";
  }

  ul li{
    list-style-type: none;
    text-decoration: none;
    padding-bottom: 3rem;
  }

  a{
    text-decoration: none;
    padding: .3rem .5rem;
    background-color: #1b82ff;
    color: white;
    font-family: "Poppins";
    cursor: pointer;
    font-size: .8rem;
    letter-spacing: .03rem;
  }

  img{
    width: 100%;
    margin-bottom: 1rem;
  }


</style>
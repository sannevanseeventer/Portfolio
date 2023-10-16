<script>
  import Nav2 from "$lib/components/Nav2.svelte";
</script>

<Nav2 />

<section>

  <div class="project1-container">

<img src="/oceancleanup.png" alt="foto van project OceanCleanup" />
<img src="/oceancleanup2.png" alt="foto van project OceanCleanup" />

<h2>Ocean Cleanup</h2>

<p>Voor GRRR, een digital agency in Amsterdam, heb ik een concept mogen ontwerpen voor The Ocean Cleanup. De bedoeling was om data van de verschillende Interceptors en hoeveelheid opgeruimd plastic zo overzichtelijk mogelijk weer te geven.</p>

<ul>
  <li><a href="www.google.com">Bekijk dashboard</a></li>
</ul>

</div>
</section>

<style>
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
    text-transform: uppercase;
    margin-bottom: 1rem;
  }

  p{
    margin-bottom: 1rem;
    font-size: 0.9rem;
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
    cursor: pointer;
    text-transform: uppercase;
    font-size: .8rem;
    font-weight: 500;
  }

  img{
    width: 100%;
    margin-bottom: 1rem;
  }


</style>
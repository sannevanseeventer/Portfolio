<script>
  import Nav2 from "$lib/components/Nav2.svelte";
</script>

<Nav2 />

<section>

  <div class="project1-container">

      <h2>Online CV</h2>

      <p>Voor mijn eindproject heb ik een online CV gebouwd waar je doorheen kan scrollen. Op deze website staat informatie over mij, mijn portfolio, ervaring en meer. Alle illustraties heb ik zelf geïllustreerd in Affinity Designer. </p>
      
      <ul>
        <li><a href="https://sannevanseeventer.nl/" target="_blank">Bekijk website</a></li>
      </ul>

<img src="/mockup-cv.webp" alt="foto van project OceanCleanup" />
<img src="/cv-2.webp" alt="foto van project OceanCleanup" />



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
  padding: .5rem;
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
<script>
</script>

<section>
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
</section>

<style>

  section {
    width: 100vw;
    height: auto;
    padding-bottom: 4rem;
    /* background-color: white; */
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


</style>

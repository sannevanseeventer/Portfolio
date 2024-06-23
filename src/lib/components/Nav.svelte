<script>

</script>

<section>
  <div class="nav-bar">
    <a href="/"><h2>Savase</h2></a>
    <!-- <img class="favicon" src="/favicon3.webp" alt="logo savase"/> -->

    <ul>
      <li><a href= #projects >Projecten</a></li>
      <li><a href="https://sannevanseeventer.nl/" target="_blank">CV</a></li>
      <li><a href=#contact><span>Contact</span></a></li>
    </ul>
  </div>
</section>

<style>

  /* .favicon{
    width: 3rem;
   margin-left: 1rem;
  } */


  h2 {
    font-family: "Bebas Neue", sans-serif;
    letter-spacing: .2rem;
    margin-left: 1rem;
    color: black;
  }

  ul {
    margin-right: 1rem;
    display: flex;
    justify-content: center;
    align-items: center;
    gap: 1.5rem;
    list-style-type: none;
  }

  ul li a {
    text-decoration: none;
    /* text-transform: uppercase; */
    color: black;
    font-family: "Poppins", sans-serif;
    letter-spacing: .05rem;
    font-size: 0.8rem;
  }

  a span{
    padding: .5rem .5rem;
    background-color:  #1273ea;
    color: white;
    text-decoration: none;
  }

  .nav-bar {
    height: 4rem;
    width: 100vw;
    background-color: white;
    position: fixed;
    height: 4rem;
    display: flex;
    justify-content: space-between;
    align-items: center;
    z-index: 1;
    border-bottom: 1px solid #e7e7e7;
  }

  .nav-bar a{
    text-decoration: none;
  }


  @media only screen and (min-width: 1024px) {

h2{
font-size: 2rem;
margin-left: 3.5rem;
}

ul {
    margin-right: 3.5rem;
    gap: 3rem;
}

ul li a {
    font-size: 1rem;
  }

  a span{
    padding: .5rem 1rem;
  }
}

</style>

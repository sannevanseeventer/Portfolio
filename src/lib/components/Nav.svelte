<script>

</script>

<section>
  <div class="nav-bar">
    <h2>Savase</h2>

    <ul>
      <li><a href="www.google.com">Projecten</a></li>
      <li><a href="www.google.com"><span>Contact</span></a></li>
    </ul>
  </div>
</section>

<style>


  h2 {
    font-family: "Bebas Neue";
    letter-spacing: .1rem;
    margin-left: 1rem;
    color: black;
  }

  ul {
    margin-right: 1rem;
    display: flex;
    justify-content: center;
    align-items: center;
    gap: 2rem;
    list-style-type: none;
  }

  ul li a {
    text-decoration: none;
    /* text-transform: uppercase; */
    color: black;
    font-family: "Poppins";
    letter-spacing: .05rem;
    font-size: 0.8rem;
  }

  a span{
    padding: .3rem .5rem;
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


  @media only screen and (min-width: 1024px) {

h2{
font-size: 2rem;
margin-left: 3rem;
}

ul {
    margin-right: 3rem;
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

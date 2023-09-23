<script>
  // import { onMount } from "svelte";
  // import { gsap } from "gsap";
  // import { ScrollTrigger } from "gsap/dist/ScrollTrigger";
  // import { Expo } from "gsap"; // Import the Expo easing functions

  // gsap.registerPlugin(ScrollTrigger);

  // // Define the toggle() and togglec() functions at the component level
  // function toggle() {
  //   tl.play();
  // }

  // function togglec() {
  //   tl.reverse();
  // }

  // let tl; // Declare the timeline variable at the component level

  // onMount(() => {
  //   tl = gsap.timeline({
  //     paused: true,
  //   });

  //   tl.to(".menu", {
  //     duration: 1,
  //     x: "0%",
  //     ease: Expo.easeInOut,
  //   });

  //   tl.fromTo(
  //     ".li",
  //     {
  //       y: "-100%",
  //       opacity: 0,
  //     },
  //     {
  //       duration: 0.5,
  //       opacity: 1,
  //       y: "0%",
  //       stagger: 0.25,
  //     }
  //   );
  // });
</script>

<section>
  <div class="nav-bar">
    <h2>Savase</h2>
    <p>menu</p>
  </div>
</section>

<!-- <section>
  <div class="container">
    <h2>Savase</h2>

    <button class="button" on:click={toggle}>menu</button>

    <div class="menu">
      <button class="button" on:click={togglec}>close</button>

      <ul class="ul">
        <li class="li1 li"><a href="www.google.com">Home</a></li>
        <li class="li2 li"><a href="www.google.com">About</a></li>
        <li class="li3 li"><a href="www.google.com">Projects</a></li>
        <li class="li4 li"><a href="www.google.com">Contact</a></li>
      </ul>
    </div>
  </div>
</section> -->

<style>
  section {
    height: 4rem;
    width: 100vw;
    background-color: white;
  }

  h2 {
    font-family: "Helvetica";
    text-transform: uppercase;
    margin-top: 1.2rem;
    margin-left: 2rem;
    color: black;
  }

  p {
    font-family: "Helvetica";
    text-transform: uppercase;
    font-size: 0.9rem;
    margin-top: 1.2rem;
    margin-right: 2rem;
    color: black;
    font-weight: 500;
  }

  .nav-bar {
    display: flex;
    justify-content: space-between;
    align-items: center;
  }
  /* * {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    font-family: "Helvetica";
  }

  .container {
    position: fixed;
    top: 0;
    left: 0;
    width: 100vw;
    height: 4rem;
    background-color: white;
  }
  .button {
    position: absolute;
    top: 1.5rem;
    right: 4rem;
    text-decoration: none;
    color: black;
    font-family: "Helvetica";
    font-size: 1rem;
    font-weight: 500;
    border: none;
    background-color: transparent;
  }

  h2 {
    font-family: "Helvetica";
    text-transform: uppercase;
    font-size: 1.5rem;
    top: 1.2rem;
    left: 2rem;
    position: absolute;
    color: black;
  }

  .menu {
    position: absolute;
    top: 0;
    left: 0;
    width: 100vw;
    height: 100vh;
    background-color: black;
    transform: translateX(-100%);
  }
  .menu .button {
    color: white;
  }
  .ul {
    position: absolute;
    left: 20%;
    display: flex;
    width: 300px;
    justify-content: center;
    align-items: left;
    height: 100vh;
    flex-direction: column;
    list-style-type: none;
  }
  .ul li {
    margin: 20px 0;
    z-index: 2;
  }
  .ul li a {
    text-decoration: none;
    color: white;
    transition: 2s;
    font-family: "Helvetica";
    font-size: 50px;
    text-transform: uppercase;
    font-weight: 600;
    mix-blend-mode: difference;
  }

  .ul li a:hover {
    transition: 2s;
    -webkit-text-fill-color: transparent;
    -webkit-text-stroke: 1px white;
    font-style: italic;
  } */
</style>

<script>
  import Queries from "../../lib/queries.svelte";
  import { fly, slide, fade } from "svelte/transition";

  let scrollValue;
</script>

<svelte:window bind:scrollY={scrollValue} />

<section class="about-section default">
    <Queries query="(min-width: 1026px)" let:matches>
        {#if matches}
          {#if scrollValue >= 350}
              <div class="about-text-box" transition:fly={{ y: 50, duration: 1300 }}>
                <h1>EXPLORE THE WORLD YOUR WAY</h1>
                <p>
                  Lorem ipsum, dolor sit amet consectetur adipisicing elit.
                  Temporibus, necessitatibus. Inventore, nam! Architecto sapiente,
                  quibusdam illum omnis rerum maxime fuga eaque inventore cum nam ea
                  consequatur tempora laudantium optio. Dignissimos.
                </p>
      
                <div class="line-style right"></div>
              </div>
      
              <img
                src="./images/mountain.jpg"
                alt=""
                class="about-img"
                transition:fly={{ x: 150, duration: 1300 }}
              />
          {/if}
        {/if}
      </Queries>
      
      <Queries query="(min-width: 481px) and (max-width: 1025px)" let:matches>
        {#if matches}
          {#if scrollValue >= 0}
              <div class="about-text-box" transition:fly={{ y: 60, duration:500 }}>
                <h1>EXPLORE THE WORLD YOUR WAY</h1>
                <p>
                  Lorem ipsum, dolor sit amet consectetur adipisicing elit.
                  Temporibus, necessitatibus. Inventore, nam! Architecto sapiente,
                  quibusdam illum omnis rerum maxime fuga eaque inventore cum nam ea
                  consequatur tempora laudantium optio. Dignissimos.
                </p>
      
                <div class="line-style right"></div>
              </div>
      
              <img
                src="./images/mountain.jpg"
                alt=""
                class="about-img"
                transition:fly={{ y: 50, duration: 1000 }}
              />
          {/if}
        {/if}
      </Queries>
      
      <Queries query="(max-width:480px)" let:matches>
        {#if matches}
      
          {#if scrollValue >= 0}
      
              <div class="about-text-box" transition:fade={{ duration: 500 }}>
                <h1>EXPLORE THE WORLD YOUR WAY</h1>
                <p>
                  Lorem ipsum, dolor sit amet consectetur adipisicing elit.
                  Temporibus, necessitatibus. Inventore, nam! Architecto sapiente,
                  quibusdam illum omnis rerum maxime fuga eaque inventore cum nam ea
                  consequatur tempora laudantium optio. Dignissimos.
                </p>
      
                <div class="line-style right"></div>
              </div>
      
              <img
                src="./images/mountain.jpg"
                alt=""
                class="about-img"
                transition:fade={{ duration: 500 }}
              />
          {/if}
      
        {/if}
       </Queries>
</section>



<!-- 320px — 480px: Mobile devices.
481px — 768px: iPads, Tablets.
769px — 1024px: Small screens, laptops.
1025px — 1200px: Desktops, large screens.
1201px and more — Extra large screens, TV. -->

<style>
  .about-section {
    position: relative;
    min-height: 80vh;
    display: flex;
    align-items: center;
    justify-content: space-between;
    flex-direction: column;
    overflow: hidden;
    background-color: #0e0d0d;
    gap: 15px;
    z-index: 1;
    padding:1em;
  }

  .about-text-box {
    position: relative;
    display: inline-block;
    min-width: 320px;
    max-width: 800px;
    text-align: center;
    margin-top: 2em;
  }

  .about-section img {
    max-width: 650px;

    border-radius: 3px;
    box-shadow: 0px 0px 10px 5px rgba(255, 255, 255, 0.253);
  }

  @media (min-width: 1200px) {
    .about-section {
      flex-direction: row;
      justify-content: space-evenly;
    }

    .about-text-box {
      margin-top: 0em;
      text-align: left;
    }
  }

  .about-text-box h1 {
    font-size: clamp(2rem, 0.5268rem + 4.7143vw, 4.0625rem);
  }

  .about-text-box p {
    font-size: clamp(1rem, 0.5982rem + 1.2857vw, 1.5625rem);
  }
</style>

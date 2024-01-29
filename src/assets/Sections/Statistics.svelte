<script>
  import Queries from "../../lib/queries.svelte";
  import { fly, slide, fade } from "svelte/transition";
  let scrollValue
</script>

<svelte:window bind:scrollY={scrollValue} />


<section class="statistics-section">
  <Queries query="(min-width: 1200px)" let:matches>
    {#if matches}
      {#if scrollValue >=1000}
        <div class="statistics-card " transition:fly={{ y: 50, duration: 1300 }}>
          <img src="./svgs/signal.svg" alt="" />
          <h3 class="stat-topic">Connected Users</h3>
          <p class="stat-num">54,325</p>
        </div>

        <div class="statistics-card" transition:fly={{ y: 50, duration: 1300 }}>
          <img src="./svgs/people.svg" alt="" />
          <h3 class="stat-topic">Satisfied Customers</h3>
          <p class="stat-num">124,325</p>
        </div> 
        <div class="statistics-card" transition:fly={{ y: 50, duration: 1300 }}>
          <img src="./svgs/mapmarker.svg" alt="" />
          <h3 class="stat-topic">Locations Traveled</h3>
          <p class="stat-num">90,324</p>
        </div>
      {/if}
    {/if}
  </Queries>

  <Queries query="(max-width: 1199px)" let:matches>
    {#if matches}
      {#if scrollValue >= 612}
      <div class="statistics-card " transition:fly={{ y: 50, duration: 1300 }}>
        <img src="./svgs/signal.svg" alt="" />
        <h3 class="stat-topic">Connected Users</h3>
        <p class="stat-num">54,325</p>
      </div>

      <div class="statistics-card" transition:fly={{ y: 50, duration: 1300 }}>
        <img src="./svgs/people.svg" alt="" />
        <h3 class="stat-topic">Satisfied Customers</h3>
        <p class="stat-num">124,325</p>
      </div> 
      <div class="statistics-card" transition:fly={{ y: 50, duration: 1300 }}>
        <img src="./svgs/mapmarker.svg" alt="" />
        <h3 class="stat-topic">Locations Traveled</h3>
        <p class="stat-num">90,324</p>
      </div>
      {/if}
    {/if}
  </Queries>


</section>

<style>
  .statistics-section {
    display: flex;
    align-items: center;
    justify-content: space-evenly;
    min-height: 50vh;
    background-color: white;
    color: black;
    font-size: clamp(1.1875rem, 0.0625rem + 2vw, 1.5625rem);
    flex-wrap:wrap;
  }

  .statistics-card {
    text-align: center;
    margin: auto;
  }

  @media (max-width: 904px) {
    .statistics-card {
      text-align: center;
      margin: 2em 0em;
    }

    .statistics-section {
       flex-direction: column;
    }
  }

  .statistics-card h3 {
    text-transform: uppercase;
    margin-top: 15px;
  }

  .statistics-card p {
    font-weight: 700;
  }

  .statistics-card img {
    width: 150px;
    height: 100px;
  }
</style>

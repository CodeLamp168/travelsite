<script>
  import Queries from "../../lib/queries.svelte";
  import { fly, slide, fade } from "svelte/transition";
  let scrollValue;

  let animationRan = false;

  function checkAndRunAnimation() {
    if (!animationRan && scrollValue >= 608) {
      animationRan = true;
      return true;
    }
    return false;
  }
</script>

<svelte:window bind:scrollY={scrollValue} />

<footer class="footer-section footer-flex">
  <Queries query="(min-width: 482px) and (max-width: 1199px)" let:matches>
    {#if matches && checkAndRunAnimation()}
      {#if scrollValue >= 508}
        <h2 transition:fly={{ y: 50, duration: 200 }}>TRAVEL.CO</h2>
        <div
          class="link-policies footer-flex"
          transition:fly={{ y: 100, duration: 100 }}
        >
          <p>info@thetravelcompany.com</p>
          <div
            class="policies footer-flex"
            transition:fly={{ y: 100, duration: 100 }}
          >
            <p>Privacy Policy</p>
            <p>Terms and Conditions</p>
          </div>
        </div>
      {/if}
    {/if}
  </Queries>

  <Queries query="(min-width:1200px)" let:matches>
    {#if matches}
      {#if scrollValue >= 1088}
        <h2 transition:fly={{ y: 50, duration: 200 }}>TRAVEL.CO</h2>
        <div
          class="link-policies footer-flex"
          transition:fly={{ y: 100, duration: 100 }}
        >
          <p>info@thetravelcompany.com</p>
          <div class="policies footer-flex">
            <p>Privacy Policy</p>
            <p>Terms and Conditions</p>
          </div>
        </div>
      {/if}
    {/if}
  </Queries>

  <Queries query="(max-width: 481px)" let:matches>
    {#if matches}
      {#if scrollValue >= 876}
        <h2 transition:fly={{ y: 50, duration: 200 }}>TRAVEL.CO</h2>
        <div
          class="link-policies footer-flex"
          transition:fly={{ y: 100, duration: 100 }}
        >
          <p>info@thetravelcompany.com</p>
          <div class="policies footer-flex">
            <p>Privacy Policy</p>
            <p>Terms and Conditions</p>
          </div>
        </div>
      {/if}
    {/if}
  </Queries>
</footer>

<!-- 
<footer class="footer-section footer-flex">


  <Queries query="(max-width: 480px)" let:matches>
    {#if matches}
      {#if scrollValue >= 1000}
        <h2>TRAVEL.CO</h2>
        <div class="link-policies footer-flex">
          <p>info@thetravelcompany.com</p>

          <div class="policies footer-flex">
            <p>Privacy Policy</p>
            <p>Terms and Conditions</p>
          </div>
        </div>
      {/if}
    {/if}
  </Queries>
</footer> -->

<style>
  .footer-flex {
    display: flex;
  }

  footer {
    flex-direction: column;
    justify-content: space-evenly;
    background: black;
    padding: 2px 3em;
    min-height: 10vh;
  }

  footer h2 {
    font-size: clamp(3.4375rem, 3.0469rem + 1.25vw, 3.75rem);
  }

  .link-policies {
    justify-content: space-between;
  }

  .policies {
    gap: 2em;
  }

  @media (max-width: 676px) {
    .footer-flex {
      justify-content: center;
      text-align: center;
      padding: 10px;
    }

    .link-policies,
    .policies {
      justify-content: center;
      flex-direction: column;
      gap: 5px;
    }
  }
</style>

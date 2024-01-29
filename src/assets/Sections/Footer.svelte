<script>

</script>

<footer class="footer-section footer-flex">
        <h2>TRAVEL.CO</h2>
        <div
          class="link-policies footer-flex"
         
        >
          <p>info@thetravelcompany.com</p>
          <div
            class="policies footer-flex"
           
          >
            <p>Privacy Policy</p>
            <p>Terms and Conditions</p>
          </div>
        </div>
</footer>


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

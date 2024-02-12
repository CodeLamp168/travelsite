<script>
 let isNavOpen = false 

const handleDropdownClick = () => {
  isNavOpen = !isNavOpen 
  console.log('click')
}


</script>

<nav>
  <div class="main-logo">
    <img src="./svgs/mountains.svg" alt="TRAVEL LOGO">
  </div>
  

  <ul class="nav-component mobile desktop" id="nav-bar" style:transform={isNavOpen ? 'translate(0%)' : 'translate(150%)'}>
    <a href="#">HOME</a>
    <a href="#">ABOUT</a>
    <a href="#">SERVICE</a>

    <button class="nav-button nav-exit" id="exit-btn" on:click={handleDropdownClick}>
      <img src="./images/nav-button-exit.svg" alt="404" />
    </button>
  </ul>

  <button class="nav-button nav-open" id="open-btn" on:click={handleDropdownClick}>
    <img src="./images/nav-button-right.svg" alt="404" />
  </button>
</nav>

<style>
  nav {
    display: flex;
    align-items: center;
    justify-content: space-between;
    width: 100%;
    padding: 10px 10px;
    position: fixed;
    z-index: 5;
    top: 0;
  }



  .main-logo {

    filter: drop-shadow(0px 0px 1px  black);
  }

  .nav-button {
    display: block;
    position: relative;
    z-index: 11;
    cursor: pointer;
    border:none;
    background:none;
    transition: transforms ease-in;
  }

  .nav-button:hover {
    transform: scale(1.1);
  }

  .nav-open {
    width: 45px;
    height: 45px;
  }

  .nav-exit {
    left:20px;
    width: 30px;
    height: 30px;
  }

  .nav-button img {
    width: 100%;
    height: auto;
  }

  .main-logo img {
    width: 100%;
    height: auto;
  }

  .nav-component {
    position: fixed;
    display: flex;
    align-items: center;
    justify-content: center;

    gap: 30px;
    z-index: 10;

    transition: transform 300ms ease-in;
  }

  .nav-component a {
    text-decoration: none;
    color: black;
    font-weight: 700;
    letter-spacing: 1px;
  }

  .mobile {
    display: flex;
    flex-direction: row;
    width: 100%;
    padding: 1em;
    background-color: #ffffff;
    gap: 20px;

    left: 0%;
    top: 0px;

    border-bottom-left-radius: 5px;
    border-bottom-right-radius: 5px;
    box-shadow: 0px 2px 3px 2px rgba(0, 0, 0, 0.479);


    z-index: 20;
  }

  /* .mobile.active {
        right:0%;
    } */

  @media (min-width: 481px) {
    .desktop {
      display: inline-flex;
      flex-direction: row;

      width: auto;
      height: auto;
      bottom: auto;
      left: auto;
      right:0;
      margin-top:5px;
 
      background: white;
      padding: 0.8em 1em;
      gap: 2em;


      border-bottom-right-radius: 0px;

      border-bottom-left-radius: 5px;
      border-top-left-radius: 5px;
      box-shadow: 0px 2px 3px 2px rgba(0, 0, 0, 0.13);

      transform: translateX(0%);
    }

    .nav-exit {
        left:0px;
    }

 

    @media (min-width: 796px) {
      .desktop {
        padding: 0.8em 2em;

        gap: 2em;
      }
    }
  }
</style>

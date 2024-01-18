<script>
</script>

<section class="header-section">
  <img src="images/mountain-header.jpg" alt="" />

  <div class="header-box">
    <h1>TRAVEL</h1>
    <p>A journey across places you never thought imagineable</p>
  </div>

  <div class="line-style left"></div>
  <div class="line-style right"></div>
</section>

<!-- 320px — 480px: Mobile devices.
481px — 768px: iPads, Tablets.
769px — 1024px: Small screens, laptops.
1025px — 1200px: Desktops, large screens.
1201px and more — Extra large screens, TV. -->

<style>
  .line-style {
    position: absolute;
    width: 120px;
    height: 3px;

    background-color: white;
  }

  .line-style.left {
    left: 20px;
    bottom: 50px;
  }

  .line-style.right {
    right: 20px;
    bottom: 50px;
  }

  /*mobile*/
  .header-section {
    position: relative;
    min-height: 320px;
    width: 100%;
    overflow: hidden;
    display: flex;
    align-items: center;
    justify-content: center;
    z-index:3;
  }

  img {
    position: absolute;
    width: 100%;
    height:100%;
    top: 0;
    border-bottom-left-radius:10px;
    border-bottom-right-radius:10px;

  }

  .header-box {
    position: relative;
    z-index: 2;
    padding: 2em;
    text-align: center;
  }

  .header-box::after {
    position: absolute;
    content: "";
    bottom: 50px;
    width: 100%;
    height: 5px;
    left: 0;
    z-index: 1;
  }

  p {
    width: 260px;
  }

  /* tablet */
  @media (min-width: 481px) {
    .header-section {
      min-height: 480px;
    }

    .line-style.left {
    left: 20px;
    bottom: 50px;
  }

  .line-style.right {
    right: 20px;
    bottom: 50px;
  }
    p {
      width: 300px;
    }
  }

  /* desktop */
  @media (min-width: 1025px) {
    .header-section {
      position: relative;
      height: 90vh;
      width: 100%;
      overflow: hidden;
      display: flex;
    }

    img {
      position: absolute;
      width: 100%;
      height: 100vh;
    }

    .header-box {
      height: 30%;
      line-height: 100px;
    }

    p {
      margin-top: 1em;
      line-height: 40px;
      width: 460px;
    }

    .line-style.left {
      left: 20px;
      bottom: 50px;
    }

    .line-style.right {
      right: 20px;
      bottom: 50px;
    }
  }

  @media (min-width: 1320px) {

    .header-section {
      position: relative;
      height: 100vh;
      width: 100%;
      overflow: hidden;
      display: flex;
    }
    .header-box {
      height: auto;
      line-height: 100px;
    }

    .line-style.left {
      left: 20px;
      bottom: 50px;
    }

    .line-style.right {
      right: 20px;
      bottom: 50px;
    }
  }

  h1 {
    font-size: clamp(3.4375rem, -15.3125rem + 33.3333vw, 9.6875rem);
    text-wrap: nowrap;
    letter-spacing: 3px;
  }
  p {
    font-size: clamp(1rem, -1.625rem + 4.6667vw, 1.875rem);
    text-transform: uppercase;
    display: inline-block;
  }
</style>

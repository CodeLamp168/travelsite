<script>

</script>



<section class="about-section">

  




    <div class="about-text-box">
        <h1>EXPLORE THE WORLD YOUR WAY</h1>
        <p>Lorem ipsum, dolor sit amet consectetur adipisicing elit. Temporibus, necessitatibus. Inventore, nam! Architecto sapiente, quibusdam illum omnis rerum maxime fuga eaque inventore cum nam ea consequatur tempora laudantium optio. Dignissimos.</p>

        <div class="line-style right"></div>
        
    </div>

    <img src="./images/mountain.jpg" alt="" class="about-img">



</section>

<!-- 320px — 480px: Mobile devices.
481px — 768px: iPads, Tablets.
769px — 1024px: Small screens, laptops.
1025px — 1200px: Desktops, large screens.
1201px and more — Extra large screens, TV. -->


<style>

    .about-section {
        position:relative;
        min-height:80vh;
        display:flex;
        align-items: center;
        justify-content:space-between;
        flex-direction: column;
        overflow:hidden;
        background-color:#0e0d0d;
        gap:15px;
        z-index:1;
    }


    .about-text-box {
        position:relative;
        display:inline-block;
        min-width:320px;
        max-width:800px;
        text-align: center;
        margin-top:2em;
    }

 
    .about-section img {

        max-width:650px;
        

        border-radius:3px;
        box-shadow:0px 0px 10px 5px rgba(255, 255, 255, 0.253);

    }

    @media(min-width:1200px){
        .about-section{
            flex-direction: row;
            justify-content:space-evenly;
        }

        .about-text-box {
            margin-top:0em;
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
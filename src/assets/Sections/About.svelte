<script>

</script>



<section class="about-section">

    <img class="about-background" src="./images/travel-img-3.jpg" alt="404">




    <div class="about-text-box">
        <h1>EXPLORE THE WORLD YOUR WAY</h1>
        <p>Lorem ipsum, dolor sit amet consectetur adipisicing elit. Temporibus, necessitatibus. Inventore, nam! Architecto sapiente, quibusdam illum omnis rerum maxime fuga eaque inventore cum nam ea consequatur tempora laudantium optio. Dignissimos.</p>
    </div>
</section>

<style>
    .about-section {
        position:relative;
        min-height:70vh;
        display:flex;
        align-items: center;
        justify-content: space-around;
        overflow:hidden;
        background-color:rgba(0, 0, 0, 0.849);
        gap:10px;
    }

    .about-background {
       position:absolute;
       opacity:0.05;
       transform:scale(1);
    }


    .about-text-box {
        display:inline-block;
        min-width:320px;
        max-width:750px;
        text-align: center;
    }

    .about-text-box h1 {
        font-size: clamp(2rem, 0.5268rem + 4.7143vw, 4.0625rem);
    }

    .about-text-box p {
        font-size: clamp(1rem, 0.5982rem + 1.2857vw, 1.5625rem);
    }
    
</style>
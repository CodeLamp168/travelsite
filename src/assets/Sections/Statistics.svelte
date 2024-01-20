<script>

</script>

<section class="statistics-section">

    <div class="statistics-card ">
        <img src="./svgs/signal.svg" alt="">
        <h3 class="stat-topic">Connected Users</h3>
        <p class="stat-num">54,325</p>
    </div>
    <div class="statistics-card ">
        <img src="./svgs/people.svg" alt="">
        <h3 class="stat-topic">Satisfied Customers</h3>
        <p class="stat-num">124,325</p>
    </div>
    <div class="statistics-card ">
        <img src="./svgs/mapmarker.svg" alt="">
        <h3 class="stat-topic">Locations Traveled</h3>
        <p class="stat-num">90,324</p>
    </div>
</section>


<style>

    .statistics-section {
        display:flex;
        align-items: center;
        justify-content: space-evenly;
        min-height:50vh;
        background-color: white;
        color:black;
        font-size:25px;
        flex-wrap: wrap;
        
    }

    .statistics-card {
        text-align: center;
        margin:auto;
    }

    @media(max-width:904px){
        .statistics-card {
        text-align: center;
        margin:2em 0em;

      }
    }

    .statistics-card h3 {
        text-transform: uppercase;
        margin-top:15px;
    }

    .statistics-card p {
        font-weight:700;
    }

    .statistics-card img {
        width:150px;
        height:100px;
    }
</style>
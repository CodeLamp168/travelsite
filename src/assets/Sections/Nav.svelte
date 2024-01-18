<script>


</script>


<nav>
    <h2>TRAVEL LOGO</h2>

    <ul class="nav-component mobile desktop">
        <a href="#">HOME</a>
        <a href="#">ABOUT</a>
        <a href="#">SERVICE</a>
    </ul>
</nav>


<style>
    nav {
        display:flex;
        align-items: center;
        justify-content: space-between;
        width:100%;
        padding:10px 10px;
        position:fixed;
        z-index:3;
        top:0;

    }

    .nav-component {
        position:fixed;
        display:flex;


        gap:30px;
        z-index:10;
    }

    .nav-component a {
        text-decoration: none;
        color:rgb(255, 255, 255);
        font-weight:700;
        letter-spacing: 1px;
    }

    .mobile {
        flex-direction: column;
        align-items: center;
        justify-content: center;
        height:100%;
        width:100%;
        background-color:#242424;

        right:-100%;
        bottom:0;

    }

    /* .mobile.active {
        right:0%;
    } */

    @media(min-width:481px){

        .desktop {
            flex-direction: row ;
            width:auto;
            height:auto;
            bottom:auto;
            right:0%;
            background-color:#24242400;

            padding-right:30px;
            gap:20px;
        }
    }

</style>
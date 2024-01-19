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
        z-index:5;
        top:0;

    }

    .nav-component {
        position:fixed;
        display:flex;
        align-items: center;
        justify-content: center;


        gap:30px;
        z-index:10;

        
    }

    .nav-component a {
        text-decoration: none;
        color:black;
        font-weight:700;
        letter-spacing: 1px;
    }


    .mobile {
        display:none;
        flex-direction: column;
        width:320px;
        padding:1em;
        background-color:#ffffff;
        gap:20px;

        left:0%;
        top:10px;;

        border-radius:10px;
        box-shadow:0px 0px 15px 2px rgba(0, 0, 0, 0.13);

        left: 50%;
        transform: translate(-50%, 0);
    }

    /* .mobile.active {
        right:0%;
    } */

    @media(min-width:481px){

        .desktop {
            display:inline-flex;
            flex-direction: row ;

            width:auto;
            height:auto;
            bottom:auto;

            left:auto;
            right:0%;
            background:white;
            padding:0.8em 1em;
            gap:2em;

            transform: translate(0%, 0);
    
        }

    @media(min-width:796px){
        .desktop {


            padding:0.8em 2em;
            margin-top:5px;
            margin-right:2em;
            gap:2em;
        }
    }
    }

</style>
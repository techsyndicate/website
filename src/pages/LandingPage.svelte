<svelte:head>
    <title>Tech Syndicate</title>
</svelte:head>
<div class="landing-div">
    <h1 class="tech">
        TECH
    </h1>
    <h1 class="syndicate">
        SYNDICATE
    </h1>
    <div class="snowglobe-assets"></div>
</div>
<div class="social-div">
    <div class="socials">
        <a href="#">
            <i class="fa-solid fa-envelope"></i>
        </a>
        <a href="#">
            <i class="fa-brands fa-instagram"></i>
        </a>
        <a href="#">
            <i class="fa-brands fa-facebook"></i>
        </a>
        <a href="#">
            <i class="fa-brands fa-behance-square"></i>
        </a>
        <a href="#">
            <i class="fa-brands fa-github"></i>
        </a>
    </div>
</div>
<style>
    .landing-div{
        height: 80vh;
        width: 100%;
    }
    .landing-div .tech,.landing-div .syndicate{
        text-align: center;
        margin-left: auto;
        margin-right: auto;
        outline: none;
    }.landing-div .tech:focus{
        outline:none;
    }
    .landing-div .tech{
        font-size: 25vw;
        font-weight: 900;
        letter-spacing: 10px;
        color: #191919;
        margin-top: 2.5vw;
    }
    .landing-div .syndicate{
        font-size: 12.5vw;
        font-weight: 900;
        letter-spacing: 5px;
        color: #16e16e;
        margin-top: -22.5vw;
    }
    .snowglobe-assets{
        height: 50vw;
        width: 50vw;
        background: url('https://media.discordapp.net/attachments/741244174736556076/973287751468339200/unknown.png?width=513&height=513');
        background-size: cover;
        background-position: center;
        display: block;
        transform: translateY(-55vw);
        margin-left: auto;
        margin-right: auto;
    }
    .social-div{
        position: absolute;
        margin-left: 70%;
        z-index: 5;
        margin-top: -6.5vw;
    }
    .socials{
        display: flex;
        width: 30vh;
        justify-content: space-between;
        font-size: 2vw;
        margin-top: .5vw;
    }
    .socials a{
        color: #fff;
        cursor: pointer;
        display: block;
        text-decoration: none;
        transition: all 0.2s ease;
    }
    .socials a:hover{
        color: #16e16e;
        transform: translateY(-5px);
    }
    .socials a::after{
        content: "";
        display: block;
        width: .25vh;
        height: 0;
        background: #fff;
        transition: all 0.2s ease;
        margin-left: auto;
        margin-right: auto;
        margin-top: .5vw;
    }
    .socials a:hover::after{
        height: 80%;
    }
    @media only screen and (max-width: 768px){
        .landing-div{
            margin-top: 50vw;
        }
        .tech{
            font-size: 30vw !important;
        }
        .syndicate {
            margin-top: -25vw !important;
            font-size:  13.5vw !important;
        }
        .snowglobe-assets{
            height: 80vw !important;
            width: 80vw !important;
            transform: translateY(-75vw) !important;
        }
        .social-div{
            margin-top: -100vw !important;
            margin-left: 15vw !important;
        }
        .socials a{
            font-size: 5vw !important;
        }
    }
</style>
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
        <a href="mailto:contact@techsyndicate.us">
            <i class="fa-solid fa-envelope"></i>
        </a>
        <a href="https://t11e.us/insta">
            <i class="fa-brands fa-instagram"></i>
        </a>
        <a href="https://t11e.us/fb">
            <i class="fa-brands fa-facebook"></i>
        </a>
        <a href="https://www.behance.net/techsyndicate">
            <i class="fa-brands fa-behance-square"></i>
        </a>
        <a href="https://t11e.us/gh">
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
        font-size: 21.5vw;
        font-weight: 900;
        letter-spacing: 10px;
        color: #191919;
        margin-top: 5vw;
    }
    .landing-div .syndicate{
        font-size: 11.5vw;
        font-weight: 900;
        letter-spacing: 5px;
        color: #16e16e;
        margin-top: -20vw;
    }
    .snowglobe-assets{
        height: 42.5vw;
        width: 42.5vw;
        background: url('https://media.discordapp.net/attachments/741244174736556076/973287751468339200/unknown.png?width=513&height=513');
        background-size: cover;
        background-position: center;
        display: block;
        transform: translateY(-47.5vw);
        margin-left: auto;
        margin-right: auto;
    }
    .social-div{
        position: absolute;
        margin-left: 70%;
        z-index: 5;
        margin-top: -5.5vw;
    }
    .socials{
        display: flex;
        width: 15vw;
        justify-content: space-between;
        font-size: 1.5vw;
        margin-top: 1.5vw; 
       
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
    @media only screen and (max-width: 1366px){
        .tech{
            margin-top:-1.5vw !important;
        }
        .socials{
            margin-top: 3.5vw !important;
        }
    }
    @media only screen and (max-width: 1920px){
        .tech{
            margin-top:-1.5vw !important;
        }
        .socials{
            margin-top: 3.5vw !important;
        }
    }
    @media only screen and (max-width: 768px){
        .landing-div{
            margin-top: 25vw;
            height: 64vh;
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
            margin-top: -20vh !important;
            margin-left: 23vw !important;
        }
        .socials{
            width: 50vw !important;
        }
        .socials a{
            font-size: 5vw !important;
        }
    }
</style>
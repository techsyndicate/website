<script></script>
<div class="landing-div">
    <div class="title">
        <h1>
            TECH
        </h1>
        <h2>
            SYNDICATE
        </h2>
    </div>
    <img src="https://media.discordapp.net/attachments/945638709007642634/947022108272230400/unknown.png?width=513&height=513" alt="">
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
    .landing-div img{
        width: 80vh;
        height: 80vh;
        object-fit: cover;
        display: block;
        margin-left: auto;
        margin-right: auto;
        margin-top: 5vw;
    }
    .title{
        text-align: center;
        margin-top: -15vw;
        position: absolute;
        font-weight: 900;
        color: #191919;
        margin-top: -26.5vw;
        z-index: -1;
        width: 100%;
    }
    .title h1{
        font-size: 31.25vw;
    }
    .title h2{
        color: #16e16e;
        font-size: 13.8vw;
        margin-top: -27.5vw;
    }
    .socials{
        display: flex;
        width: 30vh;
        display: flex;
        justify-content: space-between;
        font-size: 1.8vw;
        margin-left: 75%;
        margin-top: .5vw;
    }
    .socials a{
        color: #fff;
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
</style>
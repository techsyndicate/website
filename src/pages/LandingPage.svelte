
<div class="landing-div">
    <div class="title">
        <h1>
            TECH
        </h1>
        <h2>
            SYNDICATE
        </h2>
    </div>
    <img class="img" src="https://media.discordapp.net/attachments/945638709007642634/947022108272230400/unknown.png?width=513&height=513" alt="">
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
<script>
    import {onMount} from 'svelte'
    import gsap from 'gsap'
    import {ScrollTrigger} from 'gsap/ScrollTrigger'
    gsap.registerPlugin(ScrollTrigger)
    onMount(()=>{
        
        gsap.fromTo('.img',{
            y: 0,
        },{
            y:-250,
            duration: 2,
            scrollTrigger:{
                trigger: '.img',
                scrub: true,
                start: 'top center-=200',
            }
        })
        gsap.fromTo('.title',{
            y:0,
        },
        {
            y:-250,
            duration: 2,
            scrollTrigger:{
                trigger: '.title img',
                scrub: true,
                start: 'top center-=100',
            }
        }
        )
        gsap.fromTo('.socials',{
            y:0,
        },{
            y:-100,
            duration: 1,
            scrollTrigger:{
                trigger: '.socials',
                scrub: true,
                start: 'top center-=100',
            }
        })
    })
</script>
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
    @media only screen and (max-width: 768px){
        .img{
            width: 50vh !important;
            height: 40vh !important;
            margin-left: -7.5vw !important;
            margin-top:90vw !important;
        }
        .title{
            margin-top: -5vw !important;
            margin-left: -2.5vw !important;
        }
        .title h1{
            font-size: 38.5vw !important;
        }
        .title h2{
            font-size: 17.5vw !important;
        }
        .socials i{
            font-size: 5vw !important;
        }
        .socials {
            margin-left: 12.5vw !important;
        }
    }
</style>
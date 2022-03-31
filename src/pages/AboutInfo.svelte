<div class="about-div">
    <div class="about-img">
    </div>
    <p>
        Lorem ipsum dolor sit amet consectetur adipisicin <br>
        g elit. Et officia nihil, neque molestiae esse aliquid, <br>
        ipsam earum debitis rerum consequatur  nostrum <br>
        ducimus totam quasi facere odit. Voluptatem, dolorem.
    </p>
    <a href="#members">Meet Our Family.</a>
    <h1>Revolutionize<span style="color:#16e16e">.</span></h1>
</div>
<script>
    import {onMount} from 'svelte'
    import gsap from 'gsap'
    import { ScrollTrigger } from 'gsap/ScrollTrigger'
    gsap.registerPlugin(ScrollTrigger)
    onMount(()=>{
        gsap.fromTo('.about-img',{
            clipPath: "inset(0,0,0,0)",
        },{
            clipPath: "polygon(5% 5%, 95% 5%, 95% 95%, 5% 95%)",
            ease: "none",
            duration: 2,
            scrollTrigger: {
                trigger: '.about-div',
                start: 'top center',
                end: "top center-=200",
                scrub: true,
                anticipatePin: 1,
                anticipate: 0.5,
            }
        })
        gsap.fromTo('.about-div a',{
            opacity: 0,
            x: -20,
        },{
            opacity: 1,
            x: 0,
            ease: "none",
            duration: 1.75,
            scrollTrigger: {
                trigger: '.about-div',
                start: 'top center',
                end: "top center-=200",
                scrub: true,
                anticipatePin: 1,
                anticipate: 0.5,
            },
            delay: 1.75
        })
        gsap.fromTo('.about-div p',{
            opacity: 0,
            x: -50,
        },{
            opacity: 1,
            x: 0,
            ease: "none",
            duration: 1.75,
            scrollTrigger: {
                trigger: '.about-div',
                start: 'top center',
                end: "top center-=200",
                scrub: true,
                anticipatePin: 1,
                anticipate: 0.5,
            },
            delay: 1
        })
        gsap.fromTo('.about-div h1',{
            y: -20,
        },{
            y: 0,
            ease: "none",
            duration: 2,
            scrollTrigger: {
                trigger: '.about-div',
                start: 'top center',
                end: "bottom center-=200",
                scrub: true,
            }
        })
    })
</script>
<style>
    .about-div{
        margin-top:15vw;
        height:90vh;
        margin-left: -2.5vw;
    }

    .about-div .about-img{
        width: 125vh;
        height: 75vh;
        background: url('https://github.com/techsyndicate/website/blob/main/public/assets/images/illus-bg.png?raw=true');
        background-size: 110%;
        margin-top: -2.5vw;
        margin-left: 25vw;
        position: absolute;
        animation: reveal-1 1.5s cubic-bezier(0.77, 0, 0.175, 1);
    }
    .about-div p{
        position: absolute;
        letter-spacing: 1px;
        font-size: 1.1vw;
        letter-spacing: 0.05vw;
        line-height: 1.8vw;
        font-weight: lighter;
        margin-left: 10vw;
        margin-top: -1.5vw;
    }
    .about-div h1{
        position: absolute;
        font-size: 7.5vw;
        margin-left: 7vw;
        margin-top: 31.5vw;
    }
    .about-div a{
        position: absolute;
        font-size: 3vw;
        color: #16e16e;
        background: transparent;
        text-decoration: none;
        margin-top: 10vw;
        margin-left: 15vw;
        border:none;
        cursor: pointer;
    }
    .about-div a:before {
        content: '';
        border-bottom: solid 0.25vw #16e16e;
        position: absolute;
        bottom: -1vw; 
        left: -2.5vw;
        width: 120%; 
        transition: all 0.5s ease;
    }

    .about-div a:hover:before {
        border-bottom: solid 0.25vw #16e16e;
        transform: scale(0.5);
    }
    @media only screen and (max-width: 768px){
        .about-div{
            margin-top: -15vw !important;
        }
        .about-img,p,a{
            display: none;
        }
        .about-div h1{
            font-size: 12.5vw !important;
            margin-left: 10vw !important;
        }
    }
</style>

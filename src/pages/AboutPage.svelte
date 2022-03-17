
<div class="about" id="about">
    <h1>
        <span class="animate-this" >
            About
        </span>
        <br>
        The Club
    </h1>
    <h3>
        scroll down
    </h3>
    <div class="scroll"></div>
    <p>
        Lorem ipsum dolor sit amet consectetur adipisicin <br>
        g elit. Et officia nihil, neque molestiae esse aliquid, <br>
        ipsam earum debitis rerum consequatur  nostrum <br>
        ducimus totam quasi facere odit. Voluptatem, dolorem.
    </p>
    <img src="https://github.com/techsyndicate/website/blob/main/public/assets/images/tscircuitglow.png?raw=true" alt="">
</div>
<script>
	import {gsap} from 'gsap'
    import ScrollTrigger from 'gsap/ScrollTrigger'
    import { onMount } from "svelte";
    onMount(()=>{
        gsap.registerPlugin(ScrollTrigger)
        gsap.timeline({repeat: -1})
        gsap.fromTo('.about img',
        {
          clipPath: "inset(100%,0,0,0)",
        },
        {
          clipPath: "polygon(5% 5%, 95% 5%, 95% 95%, 5% 95%)",
          ease: "none",
          //  We want to do that animation on scroll
          scrollTrigger: {
            trigger: '.about',
            scrub: 1,
            start: "top center",
            end: "top center-=100",
          },
          duration: 2,
        },
      );
      gsap.fromTo('.scroll',{
          opacity: 0,
      },{
            opacity: 1,
            scrollTrigger: {
                trigger: '.about h1',
                scrub: 1,
                start: "top center",
                end: "top center-=100",
            },
            duration: 2,
            delay: 0.5
        })
        gsap.fromTo('h3',{
          opacity: 0,
      },{
            opacity: 1,
            scrollTrigger: {
                trigger: '.about h1 span',
                scrub: 1,
                start: "top center -=100",
            },
            duration: 2,
            delay: 1,
        })
    })
</script>
<style>
    .about{
        height: 85vh;
    }
    .about img{
        width: 100vh;
        height: 55vh;
        position: absolute;
        left: 37.5%;
        margin-top: 20.5vw;
    }
    .about h1{
        font-size: 7.5vw;
        position: absolute;
        margin-left: 5vw;
        margin-top: 2.5vw;
        color: #eee;
    }
    .about h1 span{
        color: #16e16e;
    }
    .about h3{
        text-transform: uppercase;
        letter-spacing: 1px;
        position: absolute;
        margin-left: 7.5vw;
        margin-top:50vw;
    }
    
    .scroll{
        width: 0.25vh;
        height: 27.5vh;
        position: absolute;
        background: #eee;
        margin-left: 5vw;
        margin-top: 37.5vw;
        animation: scroll 2s infinite ease;
        transition: all .5s ease;
    }
    p{
        display: none;
    }
    @keyframes scroll{
        0%{
            transform: translateY(0);
        }
        50%{
            transform: translateY(-25%);
        }
        100%{
            transform: translateY(0);
        }
    }
    @media only screen and (max-width: 768px){
        .about{
            margin-top: 27.5vw !important;
        }
        h3,.scroll{
            display: none;
        }
        h1{
            font-size: 15vw !important;
            margin-left: 2.5vw !important;
        }
        p{
            display: block;
            margin-top: 50vw;
            position: absolute;
            margin-left: 2.5vw;
        }
        img{
            transform: scale(0.45);
            margin-left: -95vw !important;
            margin-top: 65vw !important;
        }
    }
</style>
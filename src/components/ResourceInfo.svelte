
<div class="learn-div" id="learn">
    <h1>
        Learning <br>
        Resources
    </h1>
    <p>
        here you can find a variety of resources to help <br>
        you learn and excel in your chosen field
    </p>
    <img src="https://media.discordapp.net/attachments/844234171811233822/953711584461598720/Group_14.png?width=571&height=513" alt="">
    <h3>
        scroll down
    </h3>
    <div class="scroll"></div>
</div>
<div class="learn-div-mobile">
    <h1>
        Learning <br>
        Resources
    </h1>
    <p>
        here you can find a variety of resources to help <br>
        you learn and excel in your chosen field
    </p>
    <img src="https://media.discordapp.net/attachments/844234171811233822/953711584461598720/Group_14.png?width=571&height=513" alt="">
    <h3>
        scroll down
    </h3>
    <div class="scroll"></div>
</div>
<style>
    .learn-div,.learn-div-mobile{
        height: 90vh;
    }
    .learn-div-mobile{
        display: none;
    }
    h1{
        font-size: 6.5vw;
        letter-spacing:  5px;
        margin-top: 1.5%;
        margin-left: 7.5%;
    }
    img{
        position: absolute;
        margin-top: -14%;
        margin-left: 45%;
        transform: scale(1.25);
    }
    p{
        margin-left: 7.5%;
        margin-top: -2.5%;
    }
    h3{
        text-transform: uppercase;
        letter-spacing: 1px;
        position: absolute;
        margin-left: 10%;
        margin-top: 22.5%;
    }
    .scroll{
        width: 0.25vh;
        height: 22.5vh;
        position: absolute;
        background: #eee;
        margin-left: 7.5%;
        margin-top: 12.5%;
        animation: scroll 2s infinite ease;
        transition: all .5s ease;
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
    @media only screen and (max-width:768px){
        .scroll,h3{
            display: none;
        }
        h1{
            font-size: 10vw;
            letter-spacing: 1px;
        }
        .learn-div-mobile img{
            width: 38.5vh;
            margin: 10% 4.5%;
        }
        .learn-div{
            display: none;
        }
        .learn-div-mobile{
            display: block;
        }
    }
</style>
<script>
    import {gsap} from 'gsap'
    import {ScrollTrigger} from 'gsap/ScrollTrigger'
    import {onMount} from 'svelte'
    gsap.registerPlugin(ScrollTrigger)
    onMount(()=>{
        gsap.fromTo('.learn-div h1',{
            transform: 'rotate(-90deg) scale(0.1)',
            opacity: 0,
            x: -100,
        },{
            transform: 'rotate(0deg) scale(1)',
            opacity: 1,
            x: 0,
            duration: 5,
            delay: 1.5,
            ease: 'power2.inOut',
            scrollTrigger:{
                trigger: '.learn-div',
                start: 'top center',
                end: 'top center-=300',
                scrub: true,
            }
        })
        gsap.fromTo('.learn-div p',{
            transform: 'rotate(-90deg) scale(0.1)',
            opacity: 0.2,
            x: 100,
        },
        {
            transform: 'rotate(0deg) scale(1)',
            opacity: 1,
            x: 0,
            duration: 5,
            delay: 1.5,
            ease: 'power2.inOut',
            scrollTrigger:{
                trigger: '.learn-div',
                start: 'top center',
                end: 'top center-=300',
                scrub: true,
            }
        })
        gsap.fromTo('.learn-div img',{
            transform: 'rotate(-90deg) scale(0.1)',
            opacity: 0.2,
            x: 100,
        },
        {
            transform: 'rotate(0deg) scale(1)',
            opacity: 1,
            x: 0,
            duration: 7.5,
            delay: 1.5,
            ease: 'power2.inOut',
            scrollTrigger:{
                trigger: '.learn-div',
                start: 'top center',
                end: 'top center-=300',
                scrub: true,
            }
        })
        gsap.fromTo('.scroll',{
            transform: 'rotate(-75deg) scale(0.1)',
            opacity: 0.2,
            x: 100,
        },
        {
            transform: 'rotate(0deg) scale(1)',
            opacity: 1,
            x: 0,
            duration: 2,
            delay: 1.5,
            ease: 'power2.inOut',
            scrollTrigger:{
                trigger: '.learn-div',
                start: 'top center',
                end: 'top center-=300',
                scrub: true,
            }
        })
    })
</script>
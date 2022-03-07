<style>
    .current-members{
        display: flex;
        justify-content: space-between;
        width: 215%;
        height: 70vh;
        overflow-x: hidden;
        position: absolute;
        margin-top: 16.5vw;
        margin-left: 10vw;
        cursor: grab;
        transition: all .3s ease;
    }
    .current-members img{
        width: 32vh;
        height: 30vh;
        display: block;
        margin-left: auto;
        margin-right: auto;
        margin-top: 2.5vw;
        border-radius: 1vw;
    }
    .member-info{
        text-align: center;
    }
    .member-info h2{
        font-size: 2vw;
        font-weight: lighter;
    }
    .member-info h4{
        font-weight: lighter;
        color: #666;
        font-size: 1.3vw;
        margin-top: -1vw;
    }
    .card{
        width: 41.3vh;
        height:48.75vh;
        background: #191919;
        border-radius: .75vw;
        transition: all 0.5s ease;
    }
    .social-info{
        background: #393939;
        width: 55%;
        height: 3.5vh;
        border-radius: .5vw;
        margin-left: auto;
        margin-right: auto;
        margin-top: 5vw;
        transition: all 0.5s ease;
        opacity: 0;
        padding-top: 1vw;
        padding-bottom: 1vw;
    }
    .social-info a{
        color: white;
        text-decoration: none;
        font-size: 1.5vw;
        margin-left: .25vw;
        margin-right: .25vw;
    }
    .card:hover{
        height: 53.5vh;
        box-shadow: rgba(0,0,0,0.5) 0 0 10px;
    }
    .card:hover .social-info{
        margin-top: 1.5vw;
        opacity: 1;
    }
    button{
        position: absolute;
        margin-top:50vw;
        margin-left: 35%;
        background:transparent;
        font-size: 1.5vw;
        color: #eee;
        border: none;
        cursor: pointer;
        z-index: 3;
    }
    button i {
        margin-left: 1vw;
    }
    form input{
        width: 8.75vh;
        transition: all 0.5s ease;
        border: none;
        background: transparent;
        padding-bottom: .25vw;
        font-size: 1.5vw;
        position: absolute;
        margin-top: 50vw;
        margin-left: -41.5vw;
        color: #eee !important;
    }
    form input:focus{
        width: 32.5vh;
        outline: none;
        border-bottom: 0.25vw solid #16e16e;
    }
    form input::placeholder{
        color: #eee;
    }
</style>
<div class="member-info">
    <div class="current-members">
                {#each members as member}
                <div class="card" >
                    <img src="{member.pfp}" alt="{member.name}'s picture">
                    <div class="member-info">
                        <h2>{member.name}</h2>
                        <h4>{member.role}</h4>
                    </div>
                    <div class="social-info">
                        {#each member.socials as socials}
                            {#if socials.includes('instagram')}
                                <a href="{socials}" target="_blank">
                                    <i class="fa-brands fa-instagram" ></i>
                                </a>
                            {/if}
                            {#if socials.includes('facebook')}
                                <a href="{socials}" target="_blank">
                                    <i class="fa-brands fa-facebook"></i>
                                </a>
                            {/if}
                            {#if socials.includes('twitter')}
                                <a href="{socials}" target="_blank">
                                    <i class="fa-brands fa-twitter"></i>
                                </a>
                            {/if}
                        {/each}
                    </div>
                </div>
            {/each}
    </div>
    <button>
        drag <i class="fa-solid fa-arrow-right-long"></i>
    </button>
    <div class="search-input">
        <form action="">
            <input id="search" class="search" type="text" placeholder="Search by name or field">
        </form>
    </div>
</div>
<script>
    import { onMount } from 'svelte';
    import gsap from 'gsap'
    import {ScrollTrigger} from 'gsap/ScrollTrigger'
    // import Carousel from 'svelte-carousel'
    let members =[
        {
            name: "Aayan Agarwal",
            role: 'Prez',
            pfp: 'https://i.imgur.com/Rb6fHNy.png',
            socials: [
                'https://www.facebook.com/john.doe',
                'https://www.instagram.com/john.doe',
                'https://www.twitter.com/john.doe'
            ]
        },
        {
            name: "Aayush Garg",
            role: 'VP',
            pfp: 'https://i.imgur.com/Rb6fHNy.png',
            socials: [
                'https://www.facebook.com/john.doe',
                'https://www.instagram.com/john.doe',
                'https://www.twitter.com/john.doe'
            ]
        },
        {   
            name: "Yuvraaj Narula",
            role: 'Sec',
            pfp: 'https://i.imgur.com/Rb6fHNy.png',
            socials: [
                'https://www.facebook.com/john.doe',
                'https://www.instagram.com/john.doe',
                'https://www.twitter.com/john.doe'
            ]
        },
        {   
            name: "Utkarsh Dugar",
            role: 'Jt. Sec',
            pfp: 'https://i.imgur.com/Rb6fHNy.png',
            socials: [
                'https://www.facebook.com/john.doe',
                'https://www.instagram.com/john.doe',
                'https://www.twitter.com/john.doe'
            ]
        },
        {   
            name: "Nevis Kavatra",
            role: 'Core',
            pfp: 'https://i.imgur.com/Rb6fHNy.png',
            socials: [
                'https://www.facebook.com/john.doe',
                'https://www.instagram.com/john.doe',
                'https://www.twitter.com/john.doe'
            ]
        },
        {   
            name: "Amish Mamtani",
            role: 'Core',
            pfp: 'https://i.imgur.com/Rb6fHNy.png',
            socials: [
                'https://www.facebook.com/john.doe',
                'https://www.instagram.com/john.doe',
                'https://www.twitter.com/john.doe'
            ]
        },
        {   
            name: "Anirudh Chaturvedi",
            role: 'Core',
            pfp: 'https://i.imgur.com/Rb6fHNy.png',
            socials: [
                'https://www.facebook.com/john.doe',
                'https://www.instagram.com/john.doe',
                'https://www.twitter.com/john.doe'
            ]
        }
    ];
    gsap.registerPlugin(ScrollTrigger)
    onMount(()=>{
        gsap.fromTo('.card',{
            opacity: 1,
            x: 1500,
        },{
            x:0,
            duration: 1,
            scrollTrigger: {
                trigger: '.member-info',
                start: 'top center',
                end: 'top center-=100',
                anticipatePin: 1,
                anticipate: 0.5,
                scrub: true,
            }
        })
        gsap.fromTo('form',{
            opacity: 0,
            x: -100,
        },{
            opacity: 1,
            x: 0,
            duration: 1,
            delay: 1.5,
            scrollTrigger: {
                trigger: '.current-members',
                start: 'top center',
                end: 'top center-=200',
                anticipatePin: 1,
                anticipate: 0.5,
                scrub: true,
            }
        })
        gsap.fromTo('button',{
            opacity: 0,
            x: -100,
        },{
            opacity: 1,
            x: 0,
            duration: 1,
            delay: 2,
            scrollTrigger: {
                trigger: '.current-members',
                start: 'top center',
                end: 'top center-=200',
                anticipatePin: 1,
                anticipate: 0.5,
                scrub: true,
            }
        })
    })
    let search = document.querySelector('#search') 
</script>
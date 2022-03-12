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
    .card{
        width: 41.3vh;
        height: 50vh;
        background: #191919;
        border-radius: .75vw;
        transition: all 0.5s ease;
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
    .slider {
        position: absolute;
        width: 150vh;
        height: 65vh;
        top: 1.5%;
        left: 1.5%;
        padding-left: 1.5%;
        padding-right: 1%;
        overflow: hidden;
    }
    .slider-body{
        position: absolute;
        display: grid;
        height: 100%;
        top: 0;
        left: 0;
        grid-template-columns: repeat(15,1fr);
        gap: 3.5%;
        /* pointer-events: none; */
        transition: .5s ease-in;
    }
</style>
<div class="member-info">
    <div class="current-members">
        <div class="slider" id="slider">
            <div class="slider-body">
                {#each members as member}
                    <div class="card">
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
        </div>
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
            name: "Nevis Kawatra",
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
        let search = document.getElementById('search');
        search.addEventListener('keyup', ()=>{
            let searchValue = search.value.toLowerCase();
            let cards = document.querySelectorAll('.card');
            cards.forEach(card =>{
                let name = card.querySelector('h2').innerText.toLowerCase();
                let role = card.querySelector('h4').innerText.toLowerCase();
                if(name.includes(searchValue) || role.includes(searchValue)){
                    card.style.display = 'inline-block';
                }else{
                    card.style.display = 'none';
                }
            })
        })
        let draggableSlider = function () {
    let slider = document.querySelector(".slider"),
        innerSlider = document.querySelector(".slider-body");
    let pressed = false,
        startX,
        x;

    slider.addEventListener("mousedown", (e) => {
        pressed = true;
        startX = e.offsetX - innerSlider.offsetLeft;
        slider.style.cursor = "grabbing";
    });

    slider.addEventListener("mouseenter", () => {
        slider.style.cursor = "grab";
    });

    slider.addEventListener("mouseup", () => {
        slider.style.cursor = "grab";
    });

    window.addEventListener("mouseup", () => {
        pressed = false;
    });

    slider.addEventListener("mousemove", (e) => {
        if (!pressed) return;
        e.preventDefault();

        x = e.offsetX;

        innerSlider.style.left = `${x - startX}px`;

        checkBoundry();
    });

    // Check boundry of outer and inner sliders
    function checkBoundry() {
        let outer = slider.getBoundingClientRect(),
        inner = innerSlider.getBoundingClientRect();

        if (parseInt(innerSlider.style.left) > 0) {
        innerSlider.style.left = "0px";
        } else if (inner.right < outer.right) {
        innerSlider.style.left = `-${inner.width - outer.width}px`;
        }
    }
    };
    draggableSlider();
    
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
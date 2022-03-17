<div class="member-div">
    <a href="$" class="back">Return to About</a>
    <div class="toggle-title">
        <h2 id="t1" on:click="{color1}">Members</h2>
        <h2 id="t2" on:click="{color}">Alumni</h2>
    </div>
    {#if display=='block'}
        <MembersCarousel />
    {:else}
        {#if display=='none'}
            <AlumniCarousel />
        {/if}
    {/if}
</div>
<script>
    import MembersCarousel from '../components/MembersCarousel.svelte'
    import AlumniCarousel from '../components/AlumniCarousel.svelte';
    import {onMount} from 'svelte'
    import gsap from 'gsap'
    import {ScrollTrigger} from 'gsap/ScrollTrigger'
    let display ='block';
    let memberSearch = '';
    let color1=()=>{
        document.getElementById("t1").style.color="#16e16e";
        document.getElementById("t2").style.color="#333";
        display='block'
    }
    let color=()=>{
        document.getElementById("t1").style.color="#333";
        document.getElementById("t2").style.color="#16e16e";
        display='none'
    }

    onMount(()=>{
        gsap.registerPlugin(ScrollTrigger)
        gsap.fromTo('#t1',{
            fillOpacity: 0,
            x: -5,
        },{
            fillOpacity: 1,
            x: 0,
            duration: 1,
            scrollTrigger:{
                trigger: '.member-div',
                start: 'top center',
                end: 'top center-=200',
                scrub: true,
            }
        })
    })
</script>
<style>
    .member-div{
        margin-left: -5vw;
        margin-top: -.75vw;
        height: 100vh;
    }
    .back{
       color: #fff;
       text-decoration: none;
       font-size: 1.35vw;
       letter-spacing: 1px;
       position: absolute;
       margin-left: 10vw;
       margin-top: 3.5vw;
    }
    .back:before {
        content: '';
        border-bottom: solid 0.25vw #fff;
        position: absolute;
        bottom: -.5vw; 
        width: 100%; 
        transition: all 0.5s ease;
    }
    .toggle-title{
        position: absolute;
        margin-left: 10vw;
        margin-top: 2.5vw;
        display: flex;
        font-size: 4vw;
        font-weight: 900;
        letter-spacing: 1.5px;
    } 
    #t1{
        color: #16e16e;
        cursor: pointer;
    }
    #t2{
        cursor: pointer;
        margin-left: 2.5vw;
        color: #333;
    }
    @media only screen and (max-width: 768px){
        .back{
            display: none;
        }
        .member-div{
            margin-top: -110vw !important;
        }
        .toggle-title{
            font-size: 7vw !important;
            margin-left: 7.5vw !important;
        }
    }
</style>
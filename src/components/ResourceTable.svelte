<style>
    .resource-table,.resource-table-mobile{
        margin-top: 35%;
        margin-left: 7.5%;
        padding-right: 5%;
        display: grid;
        grid-template-columns: repeat(3, 1fr);
        gap: 3.5%;
    }
    .resource-card,.resource-card-mobile{
        background: #191919;
        padding: 10px;
        height: 20vh;
        width: 45vh;
        border-radius: 5px;
    }
    .resource-card p,.resource-card-mobile p{
        text-align: center;
        letter-spacing: 2px;
        font-weight: 5vw;
        margin-top: 22.5%;
        opacity: 0;
        transition: all .5 ease;
    }
    .resource-card:hover p,.resource-card-mobile:hover p{
        animation: fadeIn 1s ease;
        margin-top: 20%;
        opacity: 1;
    }
    @keyframes fadeIn {
        0% {
            opacity: 0;
        }
        100% {
            opacity: 1;
            margin-top: 20%;
        }
    }
    .resource-card img,.resource-card-mobile img{
        margin-top: -40%;
        width: 15vh;
        height: 15vw;
        margin-left: 32.5%;
    }
    .resource-card:hover img,.resource-card-mobile:hover img{
        animation: fade .5s ease;
        opacity: .2;
    }
    @keyframes fade{
        from{
            opacity: 1;
        }
        to{
            opacity: 0.2;
        }
    }
    a{
        text-decoration: none;
        color: #eee;
    }
    .resource-table-mobile{
        display: none;
    }
    @media only screen and (max-width:768px){
        .resource-table{
            display: none;
        }
        .resource-table-mobile{
            display: block;
            margin: -10% 7.5%;
        }
        .resource-card-mobile{
            width: 35vh;
            margin-bottom: 5%;
        }
        .resource-card-mobile img{
            margin-left:  27.5%;
            transform: scale(1.25);
        }
    }
</style>
<div class="resource-table">
    {#each resources as resource}
        <a href="{resource.link}" target="_blank">
            <div class="resource-card" >
                <p>{resource.field}</p>
                <img src="{resource.svg}" alt="{resource.field}'s svg">
            </div>
        </a>
    {/each}
</div>
<div class="resource-table-mobile">
    {#each resources as resource}
        <a href="{resource.link}" target="_blank">
            <div class="resource-card-mobile" >
                <p>{resource.field}</p>
                <img src="{resource.svg}" alt="{resource.field}'s svg">
            </div>
        </a>
    {/each}
</div>
<script>
    import resources from '../../data/resources.json';
    import {gsap} from 'gsap'
    import {ScrollTrigger} from 'gsap/ScrollTrigger'
    import {onMount} from 'svelte'
    gsap.registerPlugin(ScrollTrigger)
    onMount(()=>{
        gsap.fromTo('.resource-card',{
            opacity: 0,
            y: -100
        },{
            opacity: 1,
            y: 0,
            duration: 1.2,
            delay: .5,
            scrollTrigger: {
                trigger: '.resource-table',
                start: 'top center',
                end: 'top center-=200',
                scrub: true,
            }
        })
    })
</script>

<div class="event-div" id="events">
    <h1>Events</h1>
    <div class="timeline">
        {#each events as event}
            <div class="event-card">
                <h3>{event.level}</h3>
                <h1>{event.name}</h1>
            </div>
        {/each}
    </div>  
    <div class="timeline-mobile">
        {#each events as event}
            <div class="event-card">
                <h3>{event.level}</h3>
                <h1>{event.name}</h1>
            </div>
        {/each}
    </div>  
</div>
<style>
    .event-div{
        height: 90vh;
    }
    .event-div h1 {
        margin-left: 5%;
        font-size: 7.5vw;
    }
    .timeline{
        margin-top: 15vw;
    }
    .event-card{
        margin-left: 10%;
    }
    .event-card:not(:first-child){
        opacity: 0.8;
    }
    .event-card h1{
        font-weight: lighter;
        margin-top: -1.65vw;
        font-size: 5vw;
    }
    .event-card h3{
        color: #16e16e;
        font-weight: lighter;
        letter-spacing: 1px;
        margin-left: 5%;
    }
    .timeline-mobile{
        display: none;
    }
    @media only screen and (max-width: 768px){
        .timeline{
            display: none;
        }
        .timeline-mobile{
            display: block;
        }
        .event-div h1{
            font-size: 15vw;
        }
        .timeline-mobile h1{
            font-size: 7.5vw !important;
        }
        .timeline-mobile h3{
            font-size: 5vw !important;
        }
        .event-div{
            height: 50vh !important;
        }
    }
</style>
<script>
    import {gsap} from 'gsap';
    import {ScrollTrigger} from 'gsap/ScrollTrigger'
    import {onMount} from 'svelte'
    import events_details from '../../data/events.json'
    let events = events_details
    onMount(()=>{
        gsap.registerPlugin(ScrollTrigger)
        gsap.fromTo('.timeline',{
            x: '-100%',
            opacity: 0
        },{
            x: '0%',
            opacity: 1,
            scrollTrigger: {
                trigger: '#events',
                start: 'top center',
                end: 'top center-=200',
                scrub: true,
                anticipatePin: 1,
                anticipate: 0.5
            },
            duration: 1.5,
            delay: 0.6
        })
    })
</script>
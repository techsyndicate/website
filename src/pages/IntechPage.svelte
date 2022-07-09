<script>
    import events from '../../data/intech.json';
</script>
<svelte:head>
    <title>Tech Syndicate | Intech'22</title>
</svelte:head>
<meta http-equiv="refresh" content="0">

<div class="intech-div">
    <h1>inTech '22</h1>
    <p class="intech-info"> 
        Tech Syndicate, the technology club of Amity International School, Sector-46, Gurgaon, is organizing the fourth edition <br>
        of its annual intra-school event—inTech from 4th June to 20th June 2022
    </p>
    <div class="button-panel">
        <button on:click={()=>{window.location.href='/intech/guide'}}>
            Event Guide
        </button>
<!--         <button on:click={()=>{window.location.href='/intech/discord'}}>
            Discord
        </button> -->
        <button>
            Teaser
        </button>
        <button on:click="{()=>{window.location.href='/register'}}">
            Registration
        </button>
    </div>
    
    <div class="intech-events-grid">
        {#each events as event}
            <div class="event">
                <h2 class="event-name" style="padding-bottom: 12px;">{event.name}</h2>
                <p class="event-class" style="padding-bottom: 12px;"><span>Eligibility:</span> {event.class}</p>
                <p class="event-info" style="padding-bottom: 12px;">{event.info}</p>
                <br>
                <br>
                <a href="{event.link}">Prompt</a>
            </div>
        {/each}
    </div>
</div>
<style>
    .intech-div{
        width: 100%;
    }
    .intech-div h1{
        font-size: 3.5vw;
        color: #16e16e;
        margin: 2.5vw 7.5vw;
        letter-spacing:1px;
    }
    .intech-div .intech-info{
        margin-left: 7.5vw;
        font-size: 1.25vw;
    }
    .button-panel{
        margin-left: 7.5vw;
    }
    .button-panel button{
        background: #171717;
        color: #16e16e;
        font-size: 1.25vw;
        width: 10vw;
        padding: .75vw;
        border-radius: 10px;
        margin-right: 1vw;
        margin-bottom: 1vw;
        outline: none;
        cursor: pointer;
        border: none;
    }
    .intech-events-grid{
        display: grid;
        width: 100%;
        grid-template-columns: repeat(3, 28.5vw);
        margin-top: 3.5vw;
        margin-left: 7.5vw;
    }
    .event{
        border-radius: 1vw;
        background: #171717;
        transition: all .2s ease;
        height: 20vw;
        max-width: 22.5vw;
        padding: 1.5vw;
        cursor: pointer;
        margin-bottom: 3vw;
        overflow: hidden;
    }
    .event-info{
        position: absolute;
        max-width: 22.5vw;
    }
    .event-name{
        font-size: 1.5vw;
        letter-spacing: 1px;
        color: #16e16e;
    }
    .event-class span{
        color: #16e16e;
    }
    .event a {
        padding: 10px;
        background: #111;
        cursor: pointer;
        position: absolute !important;
        transition: all 0.5s ease;
        color: #16e16e;
        text-decoration: none;
        border-radius: 5px;
        margin-top: 7.5vw;
    }
    .event:hover{
        transform: translateY(-10px);
    }
    @media only screen and (max-width:768px){
        .intech-div{
            margin-top: 10vw;
        }
        .intech-div h1{
            font-size: 6.5vw;
        }
        .intech-div .intech-info{
            font-size: 4.5vw;
        }
        .intech-events-grid{
            display: block;
            width: 94%;
            margin-left: 7.5vw;
        }
        .event{
            max-width: 75vw !important;
            height: 70vw;
            border-radius: 1vw;
            margin-bottom: 5vw;
            padding: 3.5vw;
        }
        .event-name{
            font-size: 5vw;
        }
        .event-info {
            max-width: 70vw !important;
            font-size: 4vw;
            margin: -4.5vw 0.5vw;
        }
        .event a {
            margin-top: 18.5vw !important;
            font-size: 3vw;
        }
        .button-panel {
            display: flex;
        }
        .button-panel button {
            width: 25vw;
            font-size: 3.5vw;
            padding: 1.5vw;
            border-radius: 1vw;
            margin-bottom: 2.5vw;
        }
    }
</style>

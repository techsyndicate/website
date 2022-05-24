<script>
    import events from '../../data/intech.json';
</script>
<svelte:head>
    <title>Tech Syndicate | Intech'22</title>
</svelte:head>
<div class="intech-div">
    <h1>Intech'22</h1>
    <p class="intech-info"> 
        Tech Syndicate, the technology club of Amity International School, Sector-46, Gurgaon, is organizing the fourth edition <br>
        of its annual intra-school event—inTech from 4th June to 20th June 2022
    </p>
    <div class="button-panel">
        <button>
            Event Guide
        </button>
        <button>
            Discord
        </button>
        <button>
            Teaser
        </button>
        <button>
            Registration
        </button>
    </div>
    
    <div class="intech-events-grid">
        {#each events as event}
            <div class="event">
                <h2 class="event-name">{event.name}</h2>
                <p class="event-class"><span>Eligibility:</span> {event.class}</p>
                <p class="event-info">{event.info}</p>
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
        font-size: 4.5vw;
        color: #16e16e;
        margin: 2.5vw 7.5vw;
        letter-spacing:1px;
    }
    .intech-div .intech-info{
        margin-left: 8vw;
        font-size: 1.5vw;
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
            font-size: 3.25vw;
        }
        .intech-events-grid{
            display: block;
            width: 100%;
            margin-left: 7.5vw;
        }
        .event{
            max-width: 75vw !important;
            height: 65vw;
            border-radius: 1vw;
            margin-bottom: 5vw;
            padding: 3.5vw;
        }
        .event-name{
            font-size: 4vw;
        }
        .event-info {
            max-width: 70vw !important;
        }
        .event a {
            margin-top: 25vw !important;
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
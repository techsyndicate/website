<script>
    import events from '../../data/intech.json';
</script>
<svelte:head>
    <title>Tech Syndicate | Intech'22</title>
</svelte:head>
<div class="intech-div">
    <h1>Intech'22</h1>
    <p class="intech-info">
        Lorem ipsum dolor sit amet, consectetur adipiscing elit.
        Mauris eget nisl id nisl consectetur aliquam.
    </p>
    <div class="intech-events-grid">
        {#each events as event}
            <div class="event">
                <h2 class="event-name">{event.name}</h2>
                <p class="event-class"><span>Eligibility:</span> {event.class}</p>
                <p class="event-info">{event.info}</p>
                <br>
                <br>
                <a href="#">Prompt</a>
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
        transition: all 0.5s ease;
        color: #16e16e;
        text-decoration: none;
        border-radius: 5px;
    }
    .event:hover{
        transform: translateY(-10px);
    }
</style>
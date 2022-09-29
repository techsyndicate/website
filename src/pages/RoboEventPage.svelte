<script>
    import roboEvents from '../../data/robo.json';
</script>
<h1>
    Events
</h1>
<div class="robo-event-div">
    <div class="robo-grid">
        {#each roboEvents as events}
            <div class="card" style="background: {events.bg}">
                <div class="card-content">
                    <h3>
                        {events.name}
                    </h3>
                    <p style="width: 25vw;">
                        {events.description.slice(0,55)+'...'}
                    </p>
                    <p>
                        Class : {events.class}
                    </p>
                    <p>
                        Participants : {events.participants}
                    </p>
                    <a href="#">
                        Prelims
                    </a>
                </div>
                <img src="{events.icon}" alt="">
            </div>
        {/each}
    </div>
</div>
<style>
    h1{
        font-size: 5vw;
        margin: 2.5vw 5vw;
        letter-spacing: 1.5px;
    }
    .robo-event-div{
        width: 100%;
        display: flex;
        align-items: center;
        flex-direction: column;
        padding-bottom: 10vw;
        justify-content: center;
    }
    .robo-grid{
        display:grid;
        grid-template-columns: repeat(3, 31.25vw);
        margin-left: auto;
    }
    .robo-grid .card{
        border-radius: 10px;
        padding: 1.5vw;
        padding-left:2.5vw;
        padding-right: 2.5vw;
        max-width: 22.5vw;
        z-index: 2;
        overflow: hidden;
        position: relative;
        margin-right: 2vw;
        margin-top: 3.5vw;
        height: 35vw;
        transition: 0.5s;
        cursor: pointer;
    }
    .robo-grid .card:hover {
        transform: translateY(-10px);
    }
    .robo-grid .card img{
        width: 12.5vw;
        transform: rotate(10deg);
        margin: 1.5vw 15vw;
    }
    .robo-grid .card h3{
        font-size: 3vw;
    }
    .card p{
        font-size: 1.5vw;
    }
    .card a {
        position: absolute;
        margin-top: 5vw;
        padding: 10px 35px 10px 35px;
        background: rgba(0,0,0,0.1);
        border-radius: 10px;
        color: #eee;
        letter-spacing: 1px;
        font-size: 1.5vw;
        text-decoration: none;
    }
    .card-content{z-index: 2;}
    @media screen and (max-width: 768px) {
        .robo-grid{
            display: block;
            width: 95%;
        }
        h1{
            font-size: 10vw;
            margin-top: 7.5vw;
        }
        .card{
            max-width:70% !important;
            height: 55vw !important;
            margin-left: 2.5vw;
            padding: 10px !important;
        }
        .card h3{
            font-size: 7.5vw !important;
            margin: 2.5vw 2.5vw;
        }
        .card p{
            font-size: 3.5vw !important;
            width: 65vw !important;
            margin-left: 2.5vw !important;
        }
    }
</style>
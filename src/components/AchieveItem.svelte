<script>
    import { createEventDispatcher } from 'svelte';
    import {slide} from 'svelte/transition';
    export let dt;
    const dispatch=createEventDispatcher();
</script>

<div class="item" transition:slide>
    <div class="itemIn">
        <div class="dot" class:bronze={dt["pos"]=="2nd RunnerUps"} class:silver={dt["pos"]=="RunnerUps"} class:gold={dt["pos"]=="Winners"}></div>
        <div class="itemText">
            <h1 class="name">{dt["name"]}</h1>
            <h3 class="by">By {dt["host"]}</h3>
            <h3 class="pos">Overall: <span class="posType">{dt["pos"]}</span></h3>
            <div class="itemDown" on:click={()=>{dispatch('showModal',{dt:dt})}}>
                <h2 class="details">Details</h2>
                <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" fill="currentColor" class="bi bi-arrow-right" viewBox="0 0 16 16">
                    <path fill-rule="evenodd" d="M1 8a.5.5 0 0 1 .5-.5h11.793l-3.147-3.146a.5.5 0 0 1 .708-.708l4 4a.5.5 0 0 1 0 .708l-4 4a.5.5 0 0 1-.708-.708L13.293 8.5H1.5A.5.5 0 0 1 1 8z"/>
                </svg>
            </div>
        </div>
    </div>
</div>

<style>
    .item{
        background-color: #171717;
        padding: 1.5em;
        border-radius: 10px;
        padding-bottom: 0.5em;
        margin: 0.5em 0;
        transition: all 0.3s ease-in-out;
        display:flex;
        align-items: center;
        min-height: 25vh;
    }

    .itemIn{
        display:flex;
        align-items:flex-start;
    }
    .item:hover{
        margin-top: 0;
        margin-bottom: 1em;
        transition: all 0.3s ease-in-out;
    }
    .name{
        color: #16e16e;
        font-size: 1.6rem;
        margin:0;
    }
    .dot{
        width: 20px;
        height: 20px;
        background-color: #171717;
        margin-top: 0.5em;
        margin-right: 1em;
        border-radius: 100%;
    }

    .gold{background-color: #FFD700;}
    .bronze{background-color: #CD7F32;}
    .silver{background-color: #C0C0C0;}
    .by , .pos{
        color: #b2b2b2;
        font-weight: 400;
        font-size: 1rem;
    }
    .by{
        margin-bottom:0;
    }
    .pos{
        margin: 0;
    }
    .posType{
        color: #cfcfcf;
        font-weight: 600;
    }
    .details{
        font-size: 1.3rem;
        margin-bottom: 0.5em;
        font-weight: 300;
        cursor:pointer;
    }
    .itemDown{
        display:flex;
        align-items:center;
    }
    svg{
        margin-top: 0.5em;
        margin-left: 1em;
        transform: scale(1.7);
        cursor:pointer;
    }
    
    @media screen and (max-width: 600px){
        .item{
            min-height: 15vh;
        }
    }
</style>
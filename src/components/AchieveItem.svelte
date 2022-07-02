<script>
    import { createEventDispatcher } from 'svelte';
    import {slide} from 'svelte/transition';
    export let dt;
    const dispatch=createEventDispatcher();
</script>

<div class="item" transition:slide>
    <div class="itemTop">
        <div class="dot" class:bronze={dt["pos"]=="2nd RunnerUps"} class:silver={dt["pos"]=="RunnerUps"} class:gold={dt["pos"]=="Winners"}></div>
        <h1 class="name">{dt["name"]}</h1>
    </div>
    <h3 class="by">By {dt["host"]}</h3>
    <h3 class="pos">Overall <span class="posType">{dt["pos"]}</span></h3>
    <div class="itemDown" on:click={()=>{dispatch('showModal',{dt:dt})}}>
        <h2 class="details">Details</h2>
        <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" fill="currentColor" class="bi bi-arrow-right" viewBox="0 0 16 16">
            <path fill-rule="evenodd" d="M1 8a.5.5 0 0 1 .5-.5h11.793l-3.147-3.146a.5.5 0 0 1 .708-.708l4 4a.5.5 0 0 1 0 .708l-4 4a.5.5 0 0 1-.708-.708L13.293 8.5H1.5A.5.5 0 0 1 1 8z"/>
        </svg>
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
    }
    .item:hover{
        margin-top: 0;
        margin-bottom: 1em;
        transition: all 0.3s ease-in-out;
    }
    .name{
        color: #16e16e;
        font-size: 1.8rem;
        margin:0;
    }
    .itemTop{
        align-items:center;
        display:flex;
    }
    .dot{
        width: 20px;
        height: 20px;
        background-color: #171717;
        margin-right: 1em;
        border-radius: 100%;
    }

    .gold{background-color: #FFD700;}
    .bronze{background-color: #CD7F32;}
    .silver{background-color: #C0C0C0;}
    .by , .pos{
        color: #b2b2b2;
        margin-left: 0.3em;
        font-weight: 400;
    }
    .posType{
        color: #cfcfcf;
        font-weight: 600;
    }
    .details{
        margin-bottom: 0.5em;
        cursor:pointer;
    }
    .itemDown{
        display:flex;
        align-items:center;
    }
    .pos{
        margin: 0 0.3em;
    }
    svg{
        margin-top: 0.5em;
        margin-left: 1em;
        transform: scale(2);
        cursor:pointer;
    }
</style>
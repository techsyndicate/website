<script>
    import { createEventDispatcher } from 'svelte';
    const dispatch=createEventDispatcher();
</script>

<div class="item">
    <div class="itemTop">
        <div class="dot"></div>
        <h1 class="name">CW Intra</h1>
    </div>
    <h3 class="by">By DPS Vasant Kunj</h3>
    <h3 class="pos">Overall Position: <span class="posType">Winner</span></h3>
    <div class="itemDown" on:click={()=>{dispatch('showModal')}}>
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
        background-color: #FFD700;
        margin-right: 1em;
        border-radius: 100%;
    }
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
    }
</style>
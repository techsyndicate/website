<script>
    import { onMount } from 'svelte/internal';

    import AchieveItem from '../components/AchieveItem.svelte'
    let year=2022;
    let showPopup=true;
</script>

<svelte:head>
    <title>Tech Syndicate | Achievements</title>
</svelte:head>

{#if showPopup}
    <div class="modalBg">
        <div class="modal">
            <div class="top">
                <h1 class="name">CW Intra '2022</h1>
                <h2 class="by">By DPS Vasant Kink</h2>
            </div>
            <h2 class="pos">Overall RunnerUps</h2>
            <div class="events">
                <h3 class="eventName">Techathlon - 1st</h3>
                <h3 class="people">EEEEEEEEEEEEEEEEEEE, EEEEEEEEEEEEEEEEEEEEEEEEEE, EEEEEEEEEEEEEEEEE</h3>

                <h3 class="eventName">Techathlon - 1st</h3>
                <h3 class="people">EEEEEEEEEEEEEEEEEEE, EEEEEEEEEEEEEEEEEEEEEEEEEE, EEEEEEEEEEEEEEEEE</h3>

                <h3 class="eventName">Techathlon - 1st</h3>
                <h3 class="people">EEEEEEEEEEEEEEEEEEE, EEEEEEEEEEEEEEEEEEEEEEEEEE, EEEEEEEEEEEEEEEEE</h3>
            </div>
            <div class="bottom" on:click={()=>{showPopup=false;}}>
                <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" fill="currentColor" class="bi bi-arrow-left" viewBox="0 0 16 16">
                    <path fill-rule="evenodd" d="M15 8a.5.5 0 0 0-.5-.5H2.707l3.147-3.146a.5.5 0 1 0-.708-.708l-4 4a.5.5 0 0 0 0 .708l4 4a.5.5 0 0 0 .708-.708L2.707 8.5H14.5A.5.5 0 0 0 15 8z"/>
                </svg>
                Go Back
            </div>
        </div>
        
    </div>
{/if}

<div class="achievePage">
    <h1 class="title">Achievements</h1>
    <div class="menu">
        <h2 class="year" on:click={()=>{year=2022}} class:focus={year==2022}>2022</h2>
        <h2 class="year" on:click={()=>{year=2021}} class:focus={year==2021}>2021</h2>
        <h2 class="year" on:click={()=>{year=2020}} class:focus={year==2020}>2020</h2>
        <h2 class="year" on:click={()=>{year=2019}} class:focus={year==2019}>2019</h2>
    </div>
    <div class="grid">
        <AchieveItem on:showModal={()=>{showPopup=true;}}/>
        <AchieveItem />
        <AchieveItem />
        <AchieveItem />
    </div>
</div>

<style>
    .achievePage{
        padding: 1em 3em;
        margin: 0;
    }
    .title{
        font-size: 3rem;
        margin: 0;
    }
    .menu{
        display:flex;
    }
    .year:nth-child(1){
        margin-left: 0;
    }
    .year{
        margin: 1em;
        background: #171717;
        padding: 0.2em 1.5em;
        border-radius: 10px;
        font-weight:300;
    }
    .focus{
        color: #16e16e;
    }
    .grid{
        display:grid;
        grid-template-columns: 1fr 1fr 1fr;
        gap: 2em;
    }
    .modalBg{
        height: 100%;
        width: 100vw;
        background-color: rgba(0,0,0,0.5);
        position:fixed;
        display:flex;
        justify-content:center;
        z-index:200;
        margin-left: -1.5em;
        align-items: center;
        top:0;
    }
    .modal{
        width: 1000px;
        padding: 1em 2em;
        border: 2px solid #16e16e;
        background-color: #171717;
        height:max-content;
        max-width: 95vw;
        max-height: 70%;
        border-radius:20px;
        padding-bottom: 0;
    }
    .top{
        display:flex;
        align-items: center;
    }
    .name{
        color: #16e16e;
    }
    .by{
        margin-left: 0.5em;
        color: #6f6f6f;
        font-weight: 400;
    }
    .pos{
        color:#b1b1b1;
        font-weight: 600;
        margin-top:0;
    }
    .eventName{
        color: #16e16e;
        margin-bottom: 0;
    }
    .people{
        color: #dfdfdf;
        margin-top: 8px;
        margin-bottom: 2em;
    }
    .bottom{
        display:flex;
        align-items: center;
        justify-content: flex-end;
        font-size: 1.5rem;
        margin-bottom: 0.5em;
        width: 100%;
    }
    svg{
        transform: scale(2);
        margin-right: 0.5em;
        color: #16e16e;
    }
    .people:last-child{
        margin-bottom: 0.5em;
    }
</style>
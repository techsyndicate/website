<svelte:head>
    <title>Tech Syndicate | Members</title>
</svelte:head>
<script>
    import MemberGrid from '../components/MemberGrid.svelte'
    import AlumniGrid from '../components/AlumniGrid.svelte'
    import {onMount} from 'svelte';
    onMount(()=>{
        document.querySelector('#curr').addEventListener('click', ()=>{
            document.querySelector('.curr').style.display = 'block';
            document.querySelector('.alum').style.display = 'none';
            document.querySelector('#curr').classList.add('active');
            document.querySelector('#alumni').classList.remove('active');
        });
        document.querySelector('#alumni').addEventListener('click', ()=>{
            document.querySelector('.curr').style.display = 'none';
            document.querySelector('.alum').style.display = 'block';
            document.querySelector('#curr').classList.remove('active');
            document.querySelector('#alumni').classList.add('active');
        });
    })
</script>
<div class="team-div">
    <div class="team-panel">
        <div class="team-toggle">
            <button class="active" id="curr">
                Members
            </button>
            <button id="alumni">
                Alumni
            </button>
        </div>
    </div>
    <div class="curr">
        <MemberGrid />
    </div>
    <div class="alum">
        <AlumniGrid />
    </div>
</div>
<style>
    .team-div{
        width: 100%;
        height: 100vh;
    }
    .team-panel{
        width: 100%;
        display: flex;
        margin-top: 2.5vw;
    }
    .team-panel .team-toggle{
        margin-left: 5vw;
        margin-top: 1vw;
    }
    .team-panel .team-toggle button{
        background: none;
        border: none;
        outline: none;
        font-size: 2.75vw;
        color: #eee;
        cursor: pointer;
        margin-right: 2vw;
        font-weight: 600;
        letter-spacing: 1px;
    }
    .team-panel .team-toggle button.active{
        color: #16e16e;
    }
    .alum{
        display: none;
    }
    @media only screen and (max-width: 768px){
        .team-div{
            margin-top: 5vw !important;
        }
        .team-panel .team-toggle button{
            background: none;
            border: none;
            outline: none;
            font-size: 7.5vw;
            color: #eee;
            cursor: pointer;
            margin-right: 10vw;
            font-weight: 600;
            letter-spacing: 1px;
            margin-left: 1vw;
        }
        .curr,.alum{
            margin-top: 15vw !important;
        }
    }
    
</style>
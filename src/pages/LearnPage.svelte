<svelte:head>
    <title>Tech Syndicate | Resources</title>
</svelte:head>
<div class="learn-div">
    <h1>
        Learning Resources
    </h1>
    <LearnGrid />
</div>
<script>
    import LearnGrid from '../components/LearnGrid.svelte'
</script>
<style>
    .learn-div{
        width: 100%;    }
    .learn-div h1{
        font-size: 3.5vw;
        margin: 2.5vw 5vw;
        letter-spacing: 1px;
    }
    @media only screen and (max-width: 768px){
        .learn-div{
            margin-top: 12.5vw;
        }
        .learn-div h1{
            font-size: 6.5vw;
            margin-bottom: 5vw;
        }
    }
</style>
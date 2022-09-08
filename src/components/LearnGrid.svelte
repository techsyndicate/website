<script>
    import resources from '../../data/resources.json';
</script>
<div class="learn-grid">
    {#each resources as resource}
        <div class="learn-blob">
            <div class="learn-header">
                <img src="{resource.svg}" alt="{resource.field}">
                <h2 class="learn-field">
                    {resource.field}
                </h2>
            </div>
            <p>
                {resource.info}...
            </p>
            <a href="{resource.link}" target="_blank">Know more &nbsp&nbsp<i class="fa fa-arrow-right" style="padding-top: 10px;"></i>
                </a>
        </div>
    {/each}
</div>
<style>
            .fa-arrow-right:before{
            padding-top: 10px;
        }
    .learn-grid{
        display: grid;
        grid-template-columns: repeat(3, 31.25vw);
        margin: 2.5vw 5vw;
    }
    .learn-blob{
        border-radius: 10px;
        padding: 2vw;
        background: #171717;
        transition: all .2s ease;
        height: 15vw;
        width: 25vw;
        cursor: pointer;
        margin-bottom: 2vw;
    }
    .learn-blob:hover{
        transform: translateY(-5px);
    }
    .learn-header{
        display: flex;
    }
    .learn-header img{
        margin-right: 1vw;
        width: 3.5vw;
        height: 3.5vw;
        transform: translateY(1vw);
    }
    .learn-field{
        letter-spacing: 1px;
        margin-top: 2vw;
        font-size: 1.25vw;
    }
    .learn-blob p {
        color: #b5b5b5;
        font-size: 1.25vw;
        margin: 1vw 0.5vw;
    }
    .learn-blob a {
        color: #eee;
        text-decoration: none;
        font-size: 1.25vw;
        margin: -0.25vw 0.5vw;
    }
    .learn-blob a svg{
        transform: scale(0.5) translateX(1vw) translateY(1.25vw);
    }
    @media only screen and (max-width: 768px){
        .learn-grid{
            display: block;
            width: 95%;
        }
        .learn-blob{
            width: 90%;
            min-height: 45vw;
            max-height: 47.5vw;
            margin-top: 5vw;
        }
        .learn-blob img{
            width: 7.5vw !important;
            height: 7.5vw !important;
            transform: translateY(5vw) translateX(2.5vw) !important;
        }
        .learn-blob h2{
            margin-left: 5vw;
            margin-top: 6vw;
            font-size: 5vw;
        }
        .learn-blob p{
            font-size: 3.5vw;
            margin-left: 2.5vw !important;
        }
        .learn-blob a{
            font-size: 3.5vw;
            margin-left: 2.5vw;
            margin-top: 1.5vw;
        }
        .learn-blob a svg{
            transform: scale(0.5) translateX(1vw) translateY(7.5vw) !important;
            margin-bottom:2px;
        }
        .fa-arrow-right:before{
            padding-top: 10px;
        }
    }
</style>

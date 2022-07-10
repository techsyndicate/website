<svelte:head>
    <title>Tech Syndicate | About Us</title>
</svelte:head>
<div class="about-div">
    <div class="about-content">
        <h1>know us better!</h1>
        <p>
            Established in 2016, Tech Syndicate is the <br>
            technology club of Amity International School, <br>
            Sector-46, Gurgaon. The club works constantly to <br>
            encourage students to learn new technologies and <br>
            keep up with the rapidly progressing sector of <br>
            computer science.
        </p>
    </div>
    <div class="about-asset" style="text-align:center;">          
        <img src="../assets/images/resources/about.svg" alt=""> 
    </div>
</div>
<style>
    .about-div{
        width: 100%;
        display: flex;
        margin-top: -5vw;
    }
    .about-div .about-asset img{
        width: 50vw;
        margin-left: 105%;
        margin-top: 3vw;
    }
    .about-content{
        margin: 12.5vw 5vw ;
        position: absolute;
    }
    .about-content h1{
        text-transform: uppercase;
        font-size: 3.5vw;
        letter-spacing: 1px;
    }
    .about-content p {
        font-size: 1.25vw;
    }
    @media only screen and (max-width: 768px){
        .about-div{
            display: block;
        }
        .about-content{
            margin: 90vw 5vw;
        }
        .about-content h1{
            font-size: 6.5vw;
        }
        .about-content p{
            font-size: 3.5vw;
        }
        .about-div .about-asset img{
            margin-left: 5% !important;
            width: 90%;
            margin-top: 12vw !important;
        }
    }
</style>
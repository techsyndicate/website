<!-- <script>
    import Nav from '../components/Nav.svelte'
</script>
<Nav /> -->
<div class="about-div">
    <div class="about-img">
    </div>
    <p>
        Lorem ipsum dolor sit amet consectetur adipisicin <br>
        g elit. Et officia nihil, neque molestiae esse aliquid, <br>
        ipsam earum debitis rerum consequatur  nostrum <br>
        ducimus totam quasi facere odit. Voluptatem, dolorem.
    </p>
    <button>Meet Our Family.</button>
    <h1>Revolutionize<span style="color:#16e16e">.</span></h1>
</div>
<style>
    .about-div h1{
        animation: reveal 1.5s cubic-bezier(0.77, 0, 0.175, 1);
    }
    @keyframes reveal {
        0% {
            opacity: 0;
            transform: translate(0,100%);
        }
        100% {
            opacity: 1;
            transform: translate(0,0);
        }
    }
    @keyframes reveal-1{
        0% {
            opacity: 0;
            transform: translateX(100%);
        }
        100% {
            opacity: 1;
            transform: translateX(0);
        }
    }

    .about-div .about-img{
        width: 125vh;
        height: 75vh;
        background: url('https://github.com/techsyndicate/website/blob/main/public/assets/images/illus-bg.png?raw=true');
        background-size: 110%;
        margin-top: 7.5vw;
        margin-left: 26.5vw;
        position: absolute;
        animation: reveal-1 1.5s cubic-bezier(0.77, 0, 0.175, 1);
    }
    .about-div p{
        position: absolute;
        letter-spacing: 1px;
        font-size: 1.1vw;
        letter-spacing: 0.05vw;
        line-height: 1.8vw;
        font-weight: lighter;
        margin-left: 12.5vw;
        animation: reveal-1 1.5s cubic-bezier(0.77, 0, 0.175, 1);
        margin-top: 11.5vw;
    }
    .about-div h1{
        position: absolute;
        font-size: 7.5vw;
        margin-left: 8.75vw;
        margin-top: 38.5vw;
    }
    .about-div button{
        position: absolute;
        font-size: 3vw;
        color: #16e16e;
        background: transparent;
        text-decoration: none;
        margin-top: 20vw;
        animation: reveal 1.5s cubic-bezier(0.77, 0, 0.175, 1);
        margin-left: 15vw;
        border:none;
        cursor: pointer;
    }
    .about-div button:before {
        content: '';
        border-bottom: solid 0.25vw #16e16e;
        position: absolute;
        bottom: -1vw; 
        left: -2.5vw;
        width: 120%; 
        transition: all 0.5s ease;
    }

    .about-div button:hover:before {
        border-bottom: solid 0.25vw #16e16e;
        transform: scale(0.5);
    }
</style>

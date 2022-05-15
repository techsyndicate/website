<svelte:head>
    <title>Tech Syndicate | Events</title>
</svelte:head>
<script>
    import {Link} from 'svelte-navigator';
</script>
<div class="event-div">
    <h1>
        Events
    </h1>
    <div class="circle-1">
    </div>
    <div class="circle-2"></div>
    <div class="line-overlap"></div>
    <div class="circle-3"></div>
    <div class="circle-4"></div>
    <div class="circle-5"></div>
    <div class="circle-6"></div>
    <div class="line">
    </div>
    <div class="event-blob-1">
        <p class="event-name">
            Training Grounds
        </p>
        <p class="event-duration">
            Mar 12 - Apr 25
        </p>
        <br>
        <Link to = "/training" style="text-decoration: none;">
            <button>
                Join
            </button>
        </Link>
    </div>
    <div class="event-blob-2">
        <p class="event-name">
            Summer Horizon
        </p>
        <p class="event-duration">
            May 20 - May 25
        </p>
        <br>
        <Link to = "/summer" target="_blank" style="text-decoration: none;">
            <button>
                Register
            </button>
        </Link>
    </div>
    <div class="event-blob-3">
        <p class="event-name">
            Intech
        </p>
        <p class="event-duration">
            Jun 4 - Jun 20
        </p> <br>
        <Link to = "/intech" style="text-decoration: none;">
            <button>
                Explore
            </button>
        </Link>
    </div>
    <div class="event-blob-4">
        <p class="event-name">
            Robotronics
        </p>
        <p class="event-duration">
            Nov 2 - Nov 12
        </p>
    </div>
</div>
<style>
    .event-div{
        width: 100%;
        height: 65vh;
    }
    .event-div h1{
        font-size: 4.5vw;
        margin-left: 5vw;
        letter-spacing: 1px;
    }
    .line{
        width:75%;
        height: .75vw;
        border-radius: 10vw;
        background: #16e16e;
        display: block;
        margin: 15.5vw auto auto;
    }
    .line-overlap{
        width: 15%;
        height: 0.75vw;
        border-radius: 10vw;
        background: #4e4e4e;
        position: absolute;
        margin-top: 12.5vw;
        margin-left: 12.5vw;
    }
    .circle-1,
    .circle-2,
    .circle-3,
    .circle-4,
    .circle-5,.circle-6{
        background: #16e16e;
        height: 1.5vw;
        width: 1.5vw;
        position: absolute;
        border-radius:100%;
        margin-top: 12.1vw;
    }
    .circle-1 {
        margin-left: 11.5vw;
        background: #4e4e4e;
    }
    .circle-2{
        margin-left: 85%;
    }
    .circle-3{
        margin-left: 26%;
    }
    .circle-4{
        margin-left: 40.5%;
    }
    .circle-5{
        margin-left: 55%;
    }
    .circle-6{
        margin-left: 69.5%;
    }
    .event-blob-1,
    .event-blob-2,
    .event-blob-3,
    .event-blob-4{
        background: #009e45;
        position: absolute;
        width: 20vw;
        height: 8.5vw;
        border-radius: 7.5px;
    }
    .event-blob-1{
        background: #4e4e4e;
        margin: 3.5vw 15vw;
        height: 12.5vw;
    }
    .event-blob-2{
        margin: -15vw 31vw;
        height: 12.5vw;
    }
    .event-blob-3{
        margin: 3.5vw 45vw;
        height: 12.5vw;
    }
    .event-blob-4{
        margin: -15vw 61vw;
    }
    .event-name {
        font-size: 2vw;
        font-weight: 600;
        letter-spacing: 1px;
        margin-left: 1.5vw;
    }
    .event-duration{
        font-size: 1.25vw;
        font-weight: 400;
        letter-spacing: 1px;
        margin: -1.5vw 1.5vw;
    }
    .event-blob-1 button,
    .event-blob-2 button,
    .event-blob-3 button{
        font-size: 1.25vw;
        font-weight: 500;
        text-decoration: none;
        width: 10vw;
        height: 3vw;
        border-radius: 5px;
        background: #191919;
        color: #16e16e;
        padding: 10px;
        border: none;
        outline: none;
        letter-spacing: 2px;
        cursor: pointer;
        margin: 1.5vw;
    }
    @media only screen and (max-width: 768px){
        .event-div{
            margin-top: 10vw;
        }
        .event-div h1{
            font-size: 6.5vw;
        }
        .line{
            width: 1.5vw;
            height: 125vw;
        }
        .line-overlap{
            width: 1.5vw;
            height: 25vw;
            margin-left: 47.35%;
        }
        .circle-1,
        .circle-2,
        .circle-3,
        .circle-4,
        .circle-5,.circle-6{
            height: 3.5vw;
            width: 3.5vw;
            margin-left: 46.25%;
            z-index: 100;
        }
        .circle-2{
            margin-top: 35vw;
        }
        .circle-3{
            margin-top: 60vw;
        }
        .circle-4{
            margin-top: 85vw;
        }
        .circle-5{
            margin-top: 110vw;
        }
        .circle-6{
            margin-top: 135vw;
        }
        .event-blob-1,
        .event-blob-2,
        .event-blob-3,
        .event-blob-4{
            width: 35vw;
            height: 20vw;
        }
        .event-blob-1{
            margin-top: -110vw;
            margin-left: 5vw;
        }
        .event-blob-2{
            margin-top: -85vw;
            margin-left: 60vw;
        }
        .event-blob-3{
            margin-top: -60vw;
            margin-left: 5vw;
            height: 27.5vw;
        }
        .event-blob-4{
            margin-top: -35vw;
            margin-left: 60vw;
        }
        .event-name {
            font-size: 3.5vw;
            margin-left: 1.5vw;
        }
        .event-duration{
            font-size: 3vw;
            margin: -1.5vw 1.5vw;
        }
        .event-blob-3 button{
            font-size: 2.5vw;
            width: 15vw;
            height: 7.5vw;
            margin: 1.5vw;
        }

    }
</style>
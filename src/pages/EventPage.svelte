<script>
    import { Link } from "svelte-navigator";
</script>

<svelte:head>
    <title>Tech Syndicate | Events</title>
</svelte:head>
<div class="event-div" style="padding-bottom:20vh;">
    <h1 id="event-heading">Events</h1>
    <div class="circle-1"></div>
    <div class="circle-2"></div>
    <div class="circle-3"></div>
    <div class="circle-4"></div>
    <div class="circle-5"></div>
    <!-- <div class="circle-6"></div> -->
    <div class="line"></div>

    <div class="event-blob-1">
        <p class="event-name">Training Grounds</p>
        <p class="event-duration">April 8 - April 28</p>
    </div>
    <div class="event-blob-2">
        <p class="event-name">Intech</p>
        <p class="event-duration">May 18 - June 8</p>
        <br />
        <Link to="/intech" style="text-decoration: none;">
            <!-- <button>
                <span>Join</span>
            </button> -->
        </Link>
        <br />
        <!-- <Link to = "/summer" style="text-decoration: none;">
            <button>
                <span>Register</span>
            </button>
        </Link> -->
    </div>
    <div class="event-blob-3">
        <p class="event-name">Robotronics</p>
        <p class="event-duration">Oct 29 - 11 Nov</p>
        <br />
        <!-- <Link to = "/intech" style="text-decoration: none;">
            <button>
                <span>Explore</span>
            </button>
        </Link> -->
    </div>
    <!-- <div class="event-blob-4">
        <p class="event-name">
            Robotronics
        </p>
        <p class="event-duration">
            Coming Soon...
        </p>
    </div> -->
</div>

<style>
    #event-heading {
        margin-top: 5vw;
    }
    .event-div {
        width: 100%;
        height: 65vh;
        padding-bottom: 5vw;
        margin-top: -3vw;
        overflow: hidden;
    }
    .event-div h1 {
        margin-top: 1vw;
        font-size: 3.5vw;
        margin-left: 5vw;
        letter-spacing: 1px;
    }
    .line {
        width: 75%;
        height: 0.75vw;
        border-radius: 10vw;
        background: linear-gradient(
            to right,
            #16e16e 75%,
            #4e4e4e 0%,
            #4e4e4e 0%,
            #4e4e4e 100%
        );
        display: block;
        margin: 14.9vw auto auto;
    }
    /* .line-overlap{
        width: 43%;
        height: 0.75vw;
        border-radius: 10vw;
        background: #4e4e4e;
        position: absolute;
        margin-top: 12.6vw;
        margin-left: 12.5vw;
    } */
    .circle-1,
    .circle-2,
    .circle-3,
    .circle-4,
    .circle-5,
    .circle-6 {
        background: #4e4e4e;
        height: 1.5vw;
        width: 1.5vw;
        position: absolute;
        border-radius: 100%;
        margin-top: 12.1vw;
    }
    .circle-1 {
        margin-left: 11.5vw;
        background: #16e16e;
    }
    .circle-2 {
        background: #16e16e;
        margin-left: 30.2%;
        /* background: #4e4e4e; */
    }
    .circle-3 {
        background: #16e16e;
        margin-left: 48.6%;
    }
    .circle-4 {
        margin-left: 67.1%;
        background: #16e16e;
        /* background: #4e4e4e; */
    }
    .circle-5 {
        margin-left: 85.5%;
        /* background: #4e4e4e; */
    }
    .circle-6 {
        margin-left: 85.5%;
    }
    .event-blob-1,
    .event-blob-2,
    .event-blob-3,
    .event-blob-4 {
        background: #4e4e4e;
        position: absolute;
        width: 20vw;
        height: 8.5vw;
        border-radius: 7.5px;
    }
    .current {
        background-color: #009e45;
        height: 12.5vw !important;
    }
    .event-blob-1 {
        /* background: #4e4e4e; */
        margin: 3.5vw 23.5vw;
        height: 8.5vw;
    }
    .event-blob-2 {
        /* background: #4e4e4e !important; */
        margin: -13.5vw 41.5vw;
        height: 8.5vw;
    }
    .event-blob-3 {
        /* background: #4e4e4e !important; */
        margin: 3.5vw 60vw;
        height: 8.5vw;
    }
    .event-blob-4 {
        margin: -15vw 61vw;
    }
    .event-name {
        font-size: 2vw;
        font-weight: 600;
        letter-spacing: 1px;
        margin-left: 1.5vw;
    }
    .event-duration {
        font-size: 1.25vw;
        font-weight: 400;
        letter-spacing: 1px;
        margin: -1.5vw 1.5vw;
    }
    .event-blob-1 button,
    .event-blob-2 button,
    .event-blob-3 button {
        font-size: 1.25vw;
        font-weight: 500;
        text-decoration: none;
        width: 10vw;
        max-height: -3vw;
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
    @media only screen and (max-width: 1920px) {
        .event-div {
            /* margin-bottom: 30vw; */
        }
        .circle-6 {
            margin-left: 71% !important;
        }
    }
    @media only screen and (max-width: 768px) {
        .event-div {
            margin-top: 10vw;
        }
        .event-div h1 {
            font-size: 6.5vw;
        }
        .line {
            width: 1.5vw;
            height: 125vw;
            background: linear-gradient(
                to bottom,
                #16e16e 50%,
                #4e4e4e 50%
            )
                bottom;
        }
        .line-overlap {
            width: 1.5vw;
            height: 75vw;
            margin-left: 47.35%;
        }
        .circle-1,
        .circle-2,
        .circle-3,
        .circle-4,
        .circle-5,
        .circle-6 {
            height: 3.5vw;
            width: 3.5vw;
            margin-left: 46.25%;
            z-index: 90;
            background: #4e4e4e;
        }
        .circle-2 {
            margin-top: 41vw;
            background: #16e16e !important;
        }
        .circle-3 {
            background: #16e16e !important;
            margin-top: 71.5vw;
        }
        .circle-4 {
            margin-top: 102vw;
        }
        .circle-5 {
            margin-top: 132.5vw;
        }
        .circle-6 {
            margin-top: 132.5vw;
            margin-left: 46.25% !important;
        }
        .circle-1 {
            margin-top: 10vw;
            background: #16e16e !important;
        }
        .event-blob-1,
        .event-blob-2,
        .event-blob-3,
        .event-blob-4 {
            width: 40vw;
            height: 20vw;
        }
        .current {
            height: 31vw !important;
        }
        .event-blob-1 {
            margin-top: -103vw;
            margin-left: 3.5vw;
        }
        .event-blob-2 {
            margin-top: -78vw;
            margin-left: 52.5vw;
        }
        .event-blob-3 {
            margin-top: -44vw;
            margin-left: 3.5vw;
        }
        .event-blob-4 {
            margin-top: -35vw;
            margin-left: 52.5vw;
        }
        .event-name {
            font-size: 3.5vw;
            margin-left: 1.5vw;
        }
        .event-duration {
            font-size: 3vw;
            margin: -1.5vw 1.5vw;
        }
        .event-blob-3 button,
        .event-blob-1 button,
        .event-blob-2 button {
            font-size: 3vw;
            height: 10.5vw !important;
            padding: 2vw !important;
            width: 25vw;
        }
        button span {
            margin-top: -15vw !important;
            position: relative;
        }
    }
</style>

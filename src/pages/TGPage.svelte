<script>
    import { Link } from "svelte-navigator";
    import { get_slot_changes } from "svelte/internal";
    import { events } from "../../data/events.json";
</script>

<svelte:head>
    <title>Tech Syndicate | Training Grounds '23</title>
</svelte:head>

<main>
    <div class="main">
        <div class="introdiv section">
            <div class="horizontal">
                <div class="heading">
                    <h1
                        class="green headingmain"
                        style="text-align: left;margin-bottom: 20px;"
                    >
                        Training Grounds '23
                    </h1>
                </div>
                <div class="intro">
                    Welcome to Training Grounds '23, the <span class="green"
                        >second edition</span
                    >
                    of our workshop and task-based learning program. It aims to
                    <span class="green"
                        >promote learning and skill development</span
                    >
                    through a variety of authentic and guided learning experiences.
                    <br />
                </div>
                <div class="buttons">
                    <button
                        id="regbutton"
                        onclick="window.open('https://forms.gle/Tm1toPDgEFDn9Kcq5', '_blank')"
                        >Register</button
                    >
                    <a href="#events"><button>Events</button></a>
                    <a href="#dchead"><button>Discord</button></a>
                </div>
            </div>
            <div class="illus">
                <img src="../assets/images/tg.svg" alt="" />
            </div>
        </div>
        <hr />
        <div class="regbar">
            <div class="heading">
                <h1 id="dchead">Join our discord server</h1>
            </div>
            <div class="dc" id="discord">
                <div class="dcright">
                    <iframe
                        src="https://discord.com/widget?id=1091008435321065573&theme=dark"
                        width="350"
                        height="450"
                        allowtransparency="true"
                        frameborder="0"
                        sandbox="allow-popups allow-popups-to-escape-sandbox allow-same-origin allow-scripts"
                    />
                </div>
                <div class="dclef">
                    <h1>
                        Hang out with the <span class="green">community</span>
                    </h1>
                    <button
                        id="dcbutton"
                        onclick="window.open('https://discord.gg/49P3cXAc', '_blank')"
                    >
                        <img
                            src="https://www.svgrepo.com/show/353655/discord-icon.svg"
                            width="30px"
                        />
                        Server invite
                    </button>
                    <p>
                        Keep up to date with the course; all the materials,
                        workshops, and much more will happen through the discord
                        server.
                    </p>
                </div>
            </div>
        </div>
    </div>
    <hr />
    <div class="community section">
        <div class="heading">
            <h1 style="margin: 10px 0;" id="commheading">
                <span class="green">Community</span> Partners
            </h1>
        </div>
        <div class="partners">
            <div
                class="partner"
                onclick="window.open('https://www.codeday.org/', '_blank')"
            >
                <img src="../assets/images/codeday.svg" alt="" />
            </div>
            <div
                class="partner"
                onclick="window.open('https://hackclub.com/', '_blank')"
            >
                <img src="../assets/images/hackclub.svg" alt="" />
            </div>
            <div
                class="partner"
                onclick="window.open('https://www.amazonfutureengineer.com/', '_blank')"
            >
                <img src="../assets/images/amazon.svg" alt="" />
            </div>
            <div
                class="partner"
                onclick="window.open('https://gocoderz.com/', '_blank')"
            >
                <img src="../assets/images/coderz.svg" alt="" />
            </div>
            <div
                class="partner"
                onclick="window.open('https://www.autodesk.in/products/fusion-360/overview', '_blank')"
            >
                <img src="../assets/images/fusion.svg" alt="" />
            </div>
            <div
                class="partner"
                onclick="window.open('http://www.usaco.org/', '_blank')"
            >
                <img src="../assets/images/usaco.svg" alt="" />
            </div>
        </div>
    </div>
    <hr />
    <div class="heading" id="events">
        <h1>Courses</h1>
    </div>
    <div class="events section">
        {#each events as event, index}
            <div
                class="event"
                style="background-color: {event.colorHex}50;" on:click={()=>window.open(event.eventUrl, '_blank')}>
                <img src="../assets/images/resources/{event.img}" alt="" />
                <h1>{event.eventName}</h1>
                <p>{event.eventDesc}</p>
            </div>
        {/each}
    </div>
</main>

<style>
    .heading h1 {
        font-weight: bolder;
        font-size: 3rem;
        margin: 0;
        text-align: center;
    }

    .section {
        margin: 0 0 50px;
    }

    .main {
        padding: 1.5vw 2.5vw;
    }

    .introdiv {
        display: flex;
        flex-direction: row;
        justify-content: center;
        align-items: center;
        margin: 0 100px;
    }
    .horizontal {
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: start;
    }
    .intro {
        color: #999;
        font-size: 125%;
        margin-bottom: 30px;
    }

    .green {
        color: #16e16e;
    }

    .illus img {
        width: 35vw;
        margin: 20px;
    }

    .regbar {
        display: flex;
        width: 100%;
        flex-direction: column;
        justify-content: space-evenly;
        align-items: center;
    }

    button {
        background-color: #1e1e1e;
        color: #939393;
        outline: none;
        border: none;
        font-family: outfit;
        font-size: 20px;
        padding: 10px 20px;
        border-radius: 10px;
        cursor: pointer;
        margin: 10px 0;
    }

    .dclef {
        display: flex;
        flex-direction: column;
        align-items: start;
        width: 50%;
    }

    #dchead {
        text-align: center;
        color: #9e9e9e;
        font-size: 7vh;
    }

    .dclef h1 {
        margin: 0;
        font-size: 4vh;
    }

    .dclef p {
        color: #939393;
        font-size: 2.5vh;
    }

    #dcbutton {
        color: #5865f2;
        display: flex;
        justify-content: center;
        align-items: center;
    }

    #dcbutton > img {
        margin-right: 10px;
    }

    .dc {
        margin: 30px 0;
        display: flex;
        justify-content: space-evenly;
        align-items: center;
        width: 100%;
    }

    .buttons button {
        margin: 10px 20px 10px 0;
    }

    .dcright {
        margin: 20px 0;
    }
    .partners {
        display: flex;
        justify-content: center;
        align-items: center;
        flex-wrap: wrap;
        width: 70%;
        margin: 100px auto;
    }

    .partner {
        /* background-color: #ffffff09; */
        margin: 5px;
        cursor: pointer;
    }

    .partner img {
        height: 70px;
        margin: 10px;
        transition-duration: 60ms;
    }

    .partner img:hover {
        transform: scale(110%);
    }

    hr {
        border-color: #ffffff20;
        width: 70%;
        margin: 50px auto;
    }

    .events {
        display: flex;
        flex-wrap: wrap;
        width: fit-content;
        margin: 0 auto;
        justify-content: center;
    }

    .event {
        width: 300px;
        border-radius: 20px;
        margin: 20px;
        padding: 20px;
        transition-duration: 100ms;
        cursor: pointer;
    }

    .event img {
        width: 15%;
    }

    .event h1,
    .event p {
        margin: 8px;
    }

    .event:hover {
        transform: rotateZ(-2deg);
    }

    /* ? RESPONSIVE ? */
    @media only screen and (max-width: 650px) {
        .heading h1 {
            font-size: 2rem;
        }
        .intro {
            font-size: 120%;
            margin: 0px;
            margin-bottom: 30px;
        }
        .introdiv {
            margin: 0 1vw;
            margin-top: 40px;
        }
        .event {
            width: 250px;
        }

        .buttons button {
            font-size: 17px;
        }
    }
    @media only screen and (max-width: 1000px) {
        .introdiv {
            flex-direction: column;
        }
    }
    @media only screen and (max-width: 500px) {
        .buttons button {
            margin: 4vw 1vw;
            font-size: 4vw;
        }
    }
    @media only screen and (max-width: 450px) {
        .headingmain {
            font-size: 1.5rem;
        }
        .regbar {
            flex-direction: column;
        }
        .intro {
            font-size: 100%;
            margin: 0px;
            margin-bottom: 30px;
        }
        hr {
            width: 90%;
        }
    }
    @media only screen and (max-width: 900px) {
        .horizontal {
            flex-direction: column;
        }
        .illus img {
            width: 60vw;
        }
        .dc {
            flex-direction: column;
        }
        .dcright iframe {
            width: 70vw;
        }

        .dclef {
            flex-direction: column;
        }
    }
</style>

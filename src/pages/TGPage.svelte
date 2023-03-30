<script>
    import { Link } from "svelte-navigator";
</script>

<svelte:head>
    <title>Tech Syndicate | Training Grounds '23</title>
</svelte:head>

<main>
    <div class="nav">
        <div class="heading">
            <h1>Training Grounds'23</h1>
        </div>
    </div>
    <div class="main">
        <div class="introdiv section">
            <div class="horizontal">
                <div class="illus">
                    <img src="../assets/images/illus.svg" alt="" />
                </div>
                <div class="intro">
                    Training Grounds is a tech-related learning event for
                    students of Amity International School Sector 46. It offers
                    an interactive and hands-on experience in various fields. <br
                    />
                    <button id="regbutton">Register Here!</button>
                </div>
            </div>
            <hr />
            <div class="regbar">
                <div class="dc">
                    <div class="dclef">
                        <h1>
                            Hang out with the <span style="color: #16e16e;"
                                >community</span
                            >
                        </h1>
                        <button id="dcbutton"
                            ><img
                                src="https://www.svgrepo.com/show/353655/discord-icon.svg"
                                width="30px"
                            />Join the Server!</button
                        >
                    </div>
                    <div class="dcright">
                        <iframe
                            src="https://discord.com/widget?id=1091008435321065573&theme=dark"
                            width="700"
                            height="350"
                            allowtransparency="true"
                            frameborder="0"
                            sandbox="allow-popups allow-popups-to-escape-sandbox allow-same-origin allow-scripts"
                        />
                    </div>
                </div>
            </div>
        </div>
        <hr />
        <div class="community section">
            <div class="heading">
                <h1 style="margin: 10px 0;" id="commheading">Community Partners</h1>
            </div>
            <div class="partners">
                <div class="partner">
                    <img src="../assets/images/codeday.svg" alt="" />
                </div>
                <div class="partner">
                    <img src="../assets/images/hackclub.svg" alt="" />
                </div>
                <div class="partner">
                    <img src="../assets/images/amazon.svg" alt="" />
                </div>
                <div class="partner">
                    <img src="../assets/images/coderz.svg" alt="" />
                </div>
                <div class="partner">
                    <img src="../assets/images/fusion.svg" alt="" />
                </div>
                <div class="partner">
                    <img src="../assets/images/usaco.svg" alt="" />
                </div>
                </div>
            </div>
        </div>
        <div class="events section" />
</main>

<style>
    body {
        background-color: #111111;
        color: white;
        margin: 0;
    }

    .nav {
        padding: 0 30px;
        display: flex;
        justify-content: space-between;
        align-items: end;
    }

    #tsicon {
        width: 70px;
    }

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
        padding: 20px 40px;
    }

    .introdiv {
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        text-align: center;
    }
    .horizontal {
        display: flex;
        justify-content: center;
        align-items: center;
        text-align: center;
    }
    .intro {
        color: grey;
        font-size: 125%;
        margin: 0 100px;
        display: flex;
        flex-direction: column;
        align-items: center;
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
        text-align: center;
        padding: 20px 40px;
    }

    button {
        background-color: black;
        color: #16e16e;
        outline: none;
        border: none;
        font-family: outfit;
        font-size: 20px;
        padding: 10px;
        border-radius: 10px;
        cursor: pointer;
        margin: 10px 0;
    }

    .dclef {
        display: flex;
        flex-direction: row;
    }

    .dclef > * {
        margin: 10px;
    }

    #dcbutton {
        color: #5865f2;
        display: flex;
        justify-content: center;
        align-items: center;
        background-color: #23272a;
    }

    #dcbutton > * {
        margin: 0 10px;
    }

    .dc {
        margin: 30px 0;
        display: flex;
        flex-direction: column;
        justify-content: space-evenly;
        align-items: center;
        width: 100%;
    }

    .dcright {
        margin: 20px 0;
    }

    #regbutton {
        background-color: #ffffff10;
        padding: 15px;
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
    }

    .partner:hover .partners h1 {
        text-align: center;
        font-weight: 100;
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
        border-color: #ffffff50;
        width: 70%;
        margin: 50px auto;
    }

    /* ? RESPONSIVE ? */
    @media only screen and (max-width: 650px) {
        .heading h1 {
            font-size: 2rem;
        }
        .intro {
            font-size: 120%;
            margin: 0px;
        }
    }
    @media only screen and (max-width: 450px) {
        .heading h1 {
            font-size: 1.5rem;
            text-align: right;
        }
        .regbar {
            flex-direction: column;
        }
        .intro {
            font-size: 150%;
            margin: 0px;
        }
    }
    @media only screen and (max-width: 900px) {
        .horizontal {
            flex-direction: column;
        }
        .illus img {
            width: 60vw;
        }

        .intro {
            margin: 0 40px;
        }
        .dc {
            flex-direction: column;
        }
        .dcright iframe {
            width: 90vw;
        }
    }
</style>

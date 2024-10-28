<script>
  import { redirect } from "page";
  import { events } from "../../data/events.json";
  import { Notyf } from "notyf";
  var notif = new Notyf();

  function comingSoon() {
    notif.success("Revolutionizing, coming soon!");
  }
</script>

<svelte:head>
  <title>Tech Syndicate | Robotronics '24</title>
</svelte:head>

<div class="intech-div">
  <h1><span style="font-weight: 200; color: white;">Welcome to</span> <br /> <span>Robotronics '24</span></h1>
  <p class="intech-info" style="margin-bottom: 0px;">
    Robotronics '24, the <span style="color: #16e16e;">12th edition</span> of
    Tech Syndicate's annual event, will take place from
    <span style="color: #16e16e;">October 29, 2024 to November 10, 2024</span>.
    Beginning as a robotics exclusive symposium, Robotronics has now evolved and
    branched out to include events across a much wider variety of domains.
    <br /><br />
    This year it shall comprise of
    <span style="color: #16e16e;">8 events</span>
    ranging from creative, gaming to an online cryptic hunt and CTF. There
    will be one school crowned as the
    <span style="color: #16e16e;">overall winner </span>after taking into
    consideration all the 8 events.
    <br /><br /><br /><br />
  </p>
  <img alt="illus_image" src="https://i.imgur.com/fAshaQa.png" />

  <div class="button-panel">
    <div class="unspecial-buttons">
      <button
        on:click={() => {
          window.open("https://register.techsyndicate.us");
        }}
      >
        Register
      </button>
      <button
        on:click={() => {
          window.open("https://ts46.club/guide");
        }}
      >
        Brochure
      </button>
    </div>
  </div>

  <!-- <div class="intech-events-grid">
    {#each events.events as event}
      <div class="event">
        <h2 class="event-name" style="padding-bottom: 12px;">{event.name}</h2>
        <p class="event-class" style="padding-bottom: 12px;">
          <span>Eligibility:</span>
          {event.class}
        </p>
        <p class="event-info" style="padding-bottom: 12px;">{event.info}</p>
        <br />
        <br />
        <a href={event.link}>Prompt</a>
      </div>
    {/each}
  </div> -->
</div>

<main>
  <hr />
  <div class="regbar">
    <div class="heading">
      <h1 id="dchead" style="margin-left: 0px">Join our discord server</h1>
    </div>
    <div class="dc" id="discord">
      <div class="dcright">
        <iframe
          src="https://discord.com/widget?id=1277219118701084742&theme=dark"
          title="Discord"
          style="width: 30vw; height: 30vw;"
          allowtransparency="true"
          frameborder="0"
          sandbox="allow-popups allow-popups-to-escape-sandbox allow-same-origin allow-scripts"
        />
      </div>
      <div class="dclef">
        <h1>
          Hang out with the <span class="green">community</span>
        </h1>
        <p>
          Keep up to date with the event announcements and much more through the discord server.
        </p>
        <button
          id="dcbutton"
          onclick="window.open('https://techsyndicate.us/server', '_blank')"
        >
          <img
            src="https://www.svgrepo.com/show/353655/discord-icon.svg"
            width="30px"
            alt="discord"
          />
          Server invite
        </button>
      </div>
    </div>
  </div>

  <!-- <hr />
  <div class="heading">
    <h1>Trailer</h1>
  </div>
  <div class="promovideo">
    <iframe
      src="https://www.youtube.com/embed/3onxyfZ7hZc"
      title="Training Grounds &#39;24 | Opening Video"
      frameborder="0"
      allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share"
      allowfullscreen
    />
  </div> -->
  <hr />
  <div class="heading" id="events">
    <h1>Events</h1>
  </div>
  <div class="events section">
    {#each events as event, index}
      <!-- <div
        class="event"
        style="background-color: {event.colorHex}50;"
        on:click={() => comingSoon()}
      >
        <img src="../assets/images/{event.img}" alt="" />
        <h1>{event.eventName}</h1> //tg vala laga rakha hu
        <p>{event.eventDesc}</p>
      </div> -->
      <div class="eventCard" key={index}>
        <img src="../assets/images/resources/{event.img}" alt="" />
        <div class="creds">
          <h1>{event.eventName}</h1>
          <p class="info">{event.eventDesc}</p>
        </div>
        <div class="shadow"></div>
      </div>
    {/each}
  </div>
  <div class="bottom-div"></div>
</main>

<style>
  @import url("https://fonts.googleapis.com/css2?family=Outfit:wght@100..900&display=swap");
  .eventCard {
    position: inherit;
    width: 25vw;
    height: 20vw;
    flex-shrink: 0;
    border-radius: 1vw;
    background: linear-gradient(180deg, #131313 0%, #1a1a1a 100%);

    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;

    margin-bottom: 5vw;

    /* box-shadow: 0px 10px #121212; */
    /* filter: drop-shadow(0px 5px rgba(0,0,0,1)); */
    transition: all 350ms;
  }
  @media only screen and (min-width: 768px) {
    .eventCard:hover {
      margin-top: -1vw;
    }
  }
  .shadow {
    position: absolute;
    width: 24vw;
    margin-top: 1vw;
    background: #fff;
    height: 20vw;
    z-index: -10000 !important;
    border-radius: 1vw;
    background: #121212;
  }
  .creds {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
  }
  .creds h1 {
    color: #fff;
    text-align: center;
    font-family: Outfit;
    font-size: 1.2vw;
    font-style: normal;
    font-weight: 400;
    line-height: normal;
    margin-top: -0.5vw;
  }
  .info {
    color: rgba(255, 255, 255, 0.25);
    text-align: center;
    font-family: Outfit;
    font-size: 0.9vw;
    font-style: normal;
    font-weight: 400;
    line-height: normal;
    width: 20vw;
  }
  .link {
    color: #16e16e;
    text-align: center;
    font-family: Outfit;
    font-size: 1vw;
    font-style: normal;
    font-weight: 400;
    line-height: normal;
    text-decoration: none;
    cursor: pointer;
    margin-top: 0.5vw;
  }
  .eventCard img {
    width: 15vw;
    aspect-ratio: 1;
    margin-top: -9.5vw;
  }
  span {
    font-weight: 500;
  }
  .intech-div {
    width: 100%;
  }
  .intech-div h1 {
    font-size: 3.5vw;
    margin: 2.5vw 7.5vw;
    letter-spacing: 1px;
  }
  .intech-div span {
    color: #16e16e;
  }
  .intech-div .intech-info {
    margin-left: 7.5vw;
    line-height: 110%;
    font-weight: 300;
    font-size: 1.25vw;
  }
  .intech-div img {
    width: 33vw;
    float: right;
    margin-top: -30vw;
    margin-right: 7.5vw;
  }
  .intech-div p {
    margin-left: 5vw;
    font-size: 1.25vw;
    letter-spacing: 1px;
    width: 35%;
  }
  .button-panel {
    margin-left: 7.5vw;
  }
  .button-panel button {
    background: #171717;
    color: #16e16e;
    font-size: 1.25vw;
    width: 15vw;
    padding: 0.75vw;
    border-radius: 10px;
    margin-right: 1vw;
    margin-bottom: 1vw;
    outline: none;
    cursor: pointer;
    border: none;
  }
  .intech-events-grid {
    display: grid;
    width: 100%;
    grid-template-columns: repeat(3, 28.5vw);
    margin-top: 3.5vw;
    margin-left: 7.5vw;
  }
  .event {
    border-radius: 1vw;
    background: #171717;
    transition: all 0.2s ease;
    height: 20vw;
    max-width: 22.5vw;
    padding: 1.5vw;
    cursor: pointer;
    margin-bottom: 3vw;
    overflow: hidden;
  }
  .event-info {
    position: absolute;
    max-width: 22.5vw;
  }
  .event-name {
    font-size: 1.5vw;
    letter-spacing: 1px;
    color: #16e16e;
  }
  .event-class span {
    color: #16e16e;
  }
  .event a {
    padding: 10px;
    background: #111;
    cursor: pointer;
    position: absolute !important;
    transition: all 0.5s ease;
    color: #16e16e;
    text-decoration: none;
    border-radius: 5px;
    margin-top: 7.5vw;
  }
  .event:hover {
    transform: translateY(-10px);
  }

  @media only screen and (max-width: 768px) {
    .intech-div {
      margin-top: 10vw;
      display: flex;
      flex-direction: column;
    }
    .intech-div h1 {
      font-size: 6.5vw;
    }
    .intech-div .intech-info {
      font-size: 4.5vw;
    }
    .intech-div img {
      width: 50vw;
      margin: auto;
    }

    .intech-div p {
      width: 85%;
    }
    /* .intech-events-grid {
      display: block;
      width: 94%;
      margin-left: 7.5vw;
    } */
    .events {
      max-width: 75vw !important;
      /* min-height: 70vw; */
      border-radius: 1vw;
      margin-bottom: 5vw;
      margin-top: 20vw !important;
      padding: 3.5vw;
      gap: 40vw !important;
    }
    #dchead {
      margin: 0;
    }
    .dclef {
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
    }
    .eventCard {
      transform: scale(1.7);
      z-index: 2;
      box-shadow: 0 1.5vw 0 -1vw #121212;
      animation: none;
      transition: none;
    }
    .eventCard:hover {
      z-index: 4;
    }
    .shadow {
      display: none;
    }

    .eventCard {
      width: 36vw;
      height: 40vw;
      border-radius: 24px;
      margin-top: 7vw;
    }
    .shadow {
      width: 34vw;
      margin-top: 2vw;
      height: 40vw;
      border-radius: 12.6px;
    }
    .eventCard img {
      width: 30vw;
      margin-top: -15vw;
    }
    .eventCard .creds p {
      width: 30vw;
    }
    .eventCard .creds > h1,
    .eventCard .creds > a,
    .eventCard .creds > p {
      font-size: 2vw !important;
    }
    .event-name {
      font-size: 5vw;
    }
    .event-info {
      max-width: 70vw !important;
      font-size: 4vw;
      margin: -4.5vw 0.5vw;
    }
    .event a {
      margin-top: 18.5vw !important;
      font-size: 3vw;
    }
    .button-panel {
      display: flex;
      justify-content: center;
      margin-left: 0px;
      margin-top: 5vw;
    }
    .button-panel button {
      width: 35vw;
      font-size: 3.5vw;
      padding: 1.5vw;
      border-radius: 1vw;
      margin-bottom: 2.5vw;
    }
  }
  .heading h1 {
    font-weight: bolder;
    font-size: 3rem;
    margin: 0;
    /* text-align: center; */
    margin-left: 7.7vw;
    margin-top: 4.5vw;
    margin-bottom: 4.5vw !important;
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
    color: #fff;
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
    color: #fff;
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
    align-items: flex-start;
    width: 30vw;
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
    /* width: 50vw; */
    display: flex;
    align-items: end;
    justify-content: center;
  }
  .partners {
    display: flex;
    justify-content: center;
    align-items: center;
    flex-wrap: wrap;
    width: 60%;
    margin: 100px auto;
  }

  .partner {
    margin: 5px;
    cursor: pointer;
  }

  .partner img {
    height: 6vh;
    margin: 5px;
    transition-duration: 60ms;
  }

  .partner img:hover {
    transform: scale(110%);
  }

  hr {
    border-color: #ffffff20;
    width: 85%;
    margin: 50px auto;
  }

  .events {
    display: flex;
    flex-wrap: wrap;
    width: fit-content;
    margin: 5vw auto;
    justify-content: center;
    gap: 4.3vw;
  }

  .event {
    width: 20vw;
    height: 220px;
    border-radius: 20px;
    margin: 20px;
    padding: 20px;
    transition-duration: 100ms;
    cursor: pointer;
  }

  .event img {
    width: 15%;
  }

  .promovideo {
    margin: 50px auto;
    width: fit-content;
  }

  .promovideo iframe {
    width: 80vw;
    height: calc(80vw * 580 / 1031);
  }

  .promovideo {
    margin: 50px auto;
    width: fit-content;
  }

  .promovideo iframe {
    width: 80vw;
    height: calc(80vw * 580 / 1031);
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
    /* #dcbutton {
      display: none;
    } */
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
    /* .introdiv {
      flex-direction: column;
    } */
  }
  @media only screen and (max-width: 500px) {
    /* .buttons button {
      margin: 4vw 1vw;
      font-size: 4vw;
    } */
    /* .bottom-div {
      width: 100%;
      height: 50vh;
    } */
    .events {
      gap: 60vw !important;
      margin: 33vw auto !important;
      /* padding: 20vw; */
    }
    .eventCard {
      transform: scale(2);
      z-index: 2;
      box-shadow: 0 1.5vw 0 -1vw #121212;
      animation: none;
      transition: none;
    }
    .eventCard:hover {
      z-index: 4;
    }
    .shadow {
      display: none;
    }
    .button-panel button {
      margin-right: 3vw;
      padding: 3vw;
      margin-bottom: 10vw;
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
    .dclef h1 {
      font-size: 3vh;
    }
  }
  @media only screen and (max-width: 900px) {
    .dclef {
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      margin-top: 10vw;
    }
    .horizontal {
      flex-direction: column;
    }
    .illus img {
      width: 100vw;
      left: -5vw;
      position: relative;
    }
    .dc {
      flex-direction: column;
    }
    .dcright iframe {
      width: 80vw !important;
      height: 40vh !important;
    }
    .dclef {
      flex-direction: column;
      width: 90%;
      text-align: center !important;
    }
    #dchead {
      font-size: 5vh;
    }
  }
</style>

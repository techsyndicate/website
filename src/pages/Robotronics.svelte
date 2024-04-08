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
  <title>Tech Syndicate | Training Grounds '24</title>
</svelte:head>

<!-- <div class="intech-div">
  <h1>Welcome to <br /> <span>Robotronics '23</span></h1>
  <p class="intech-info">
    Robotronics '23, the <span style="color: #16e16e;">10th edition</span> of
    Tech Syndicate's annual event, will take place from
    <span style="color: #16e16e;">October 20, 2023 to November 3, 2023</span>.
    Beginning as a robotics exclusive symposium, Robotronics has now evolved and
    branched out to include events across a much wider variety of domains.
    <br /><br />
    This year it shall comprise of
    <span style="color: #16e16e;">14 events</span>
    ranging from creative, robotics to an online cryptic hunt and crossword. There
    will be one school crowned as the
    <span style="color: #16e16e;">overall winner </span>after taking into
    consideration all the 14 events.
    <br /><br /><br /><br />
  </p>
  <img src="../assets/images/events.png" />

  <div class="button-panel">
    <button
      on:click={() => {
        window.location.href = "/guide";
      }}
    >
      Event Guide
    </button>
    <button
      on:click={() => {
        window.location.href = "/server";
      }}
    >
      Discord
    </button>
    <button
      on:click={() => {
        window.location.href = "https://register.techsyndicate.us";
      }}
    >
      Registration
    </button>
  </div>

  <div class="intech-events-grid">
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
  </div>
</div> -->

<main>
  {#if window.innerWidth > 600}
  <div class="intech-div">
    <h1>Welcome to <br /> <span style="font-weight: 700;">Training Grounds '24</span></h1>
    <p class="intech-info">
      Training Grounds '24, the <span style="color: #16e16e;">3rd edition</span> of our workshop and task-based learning program will take place from
      <span style="color: #16e16e;">April 8 to April 28</span>.
      It aims to promote learning and
      <span style="color: #16e16e;">skill development </span>through a variety of authentic and guided learning experiences. This year it shall comprise of <span style="color: #16e16e;">10 workshops</span> ranging from design, development, cryptography and crossword.
      <br /><br />
    </p>
    <div class="button-panel">
      <button
        on:click={() => {
          // comingSoon()
          // window.location.href="https://forms.gle/Kgn3ZXuBv58YCJPc8"
          window.open('https://forms.gle/Kgn3ZXuBv58YCJPc8', '_blank', 'noopener, noreferrer');
        }}
      >
      Registration
    </button>
    <button
    on:click={() => {
      // comingSoon()
      window.open('https://discord.gg/3AeWKvUGDc', '_blank', 'noopener, noreferrer');
      
    }}
      >
      Discord
    </button>
    <button
    on:click={() => {
      window.open('https://chat.whatsapp.com/IrfgAUMusLyDZar7CYNpJD', '_blank', 'noopener, noreferrer');
        }}
      >
        WhatsApp
      </button>
    </div>
    <img alt="illus_img" src="https://i.imgur.com/fAshaQa.png" />
  </div>
  {:else}
  <div class="intech-div">
    <h1>Welcome to <br /> <span style="font-weight: 700;">Training Grounds '24</span></h1>
    <p class="intech-info">
      Training Grounds '24, the <span style="color: #16e16e;">3rd edition</span> of our workshop and task-based learning program will take place from
      <span style="color: #16e16e;">April 8 to April 28</span>.
      It aims to promote learning and
      <span style="color: #16e16e;">skill development </span>through a variety of authentic and guided learning experiences. This year it shall comprise of <span style="color: #16e16e;">10 workshops</span> ranging from design, development, cryptography and crossword.
      <br /><br />
    </p>
    <div class="button-panel">
      <button
        on:click={() => {
          // comingSoon()
          // window.location.href="https://forms.gle/Kgn3ZXuBv58YCJPc8"
          // window.open(
          //   'https://forms.gle/Kgn3ZXuBv58YCJPc8',
          //   "_blank" // <- This is what makes it open in a new window.
          // );
          window.open('https://forms.gle/Kgn3ZXuBv58YCJPc8', '_blank', 'noopener, noreferrer');
        }}
      >
        Registration
      </button>
      <button
        on:click={() => {
          window.open('https://discord.gg/3AeWKvUGDc', '_blank', 'noopener, noreferrer');
          
        }}
      >
        Discord
      </button>
      <button
        on:click={() => {
          window.open('https://chat.whatsapp.com/IrfgAUMusLyDZar7CYNpJD', '_blank', 'noopener, noreferrer');
          
        }}
      >
        WhatsApp
      </button>
    </div>
    <img alt="illus_image" src="https://i.imgur.com/fAshaQa.png" />
  </div>
  {/if}
  
  <!-- <hr /> -->
  <!-- <div class="regbar">
    <div class="heading">
      <h1 id="dchead">Join our discord server</h1>
    </div>
    <div class="dc" id="discord">
      <div class="dcright">
        <iframe
          src="https://discord.com/widget?id=1155922275942543372&theme=dark"
          width="350"
          title="Discord"
          height="400"
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
          Keep up to date with the event announcements and <br />
          much more through the discord server.
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
  </div> -->

  <!-- <hr />
  <div class="heading">
    <h1>Trailer</h1>
  </div>
  <div class="promovideo">
    <iframe
      src="https://www.youtube.com/embed/3onxyfZ7hZc"
      title="Training Grounds &#39;23 | Opening Video"
      frameborder="0"
      allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share"
      allowfullscreen
    />
  </div> -->
  <!-- <hr /> -->
  <div class="heading" id="events">
    <h1>Workshops</h1>
  </div>
  <div class="events section">
    {#each events as event, index}
      <!-- <div
        class="event"
        style="background-color: {event.colorHex}50;"
        on:click={() => comingSoon()}
      >
        <img src="../assets/images/{event.img}" alt="" />
        <h1>{event.eventName}</h1>
        <p>{event.eventDesc}</p>
      </div> -->
      <div class="eventCard">
        <img src="../assets/images/resources/{event.img}" alt="">
        <div class="creds">
          <h1>{event.eventName}</h1>
          <p class="info">{event.eventDesc}</p>
          <a href="{event.eventUrl}" target="_blank" class="link">Learn More</a>
        </div>
        <div class="shadow">
        </div>
      </div>
      {/each}
    </div>
    <!-- <div style="width: 100%; height: 50vh" class="">

    </div> -->
</main>

<style>
  @import url('https://fonts.googleapis.com/css2?family=Outfit:wght@100..900&display=swap');
  .eventCard {
    position: inherit;
    width: 18vw;
    height: 20vw;
    flex-shrink: 0;
    border-radius: 1vw;
    background: linear-gradient(180deg, #131313 0%, #1A1A1A 100%);
    
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    
    margin-bottom: 5vw;
    
    /* box-shadow: 0px 10px #121212; */
    /* filter: drop-shadow(0px 5px rgba(0,0,0,1)); */
    transition: all 350ms ;
  }
  @media only screen and (min-width: 768px) {
    .eventCard:hover {
      margin-top: -1vw;
    }
  }
  .shadow {
    position: absolute;
    width: 17vw;
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
    color: #FFF;
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
    width: 15vw;
  }
  .link {
    color: #16E16E; 
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
    margin-top: -7vw;
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
    margin-top: -25vw;
    margin-right: 10vw;
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
    width: 10vw;
    padding: 0.75vw;
    border-radius: 10px;
    margin-right: 1vw;
    margin-bottom: 1vw;
    outline: none;
    cursor: pointer;
    border: none;
  }
  /* .intech-events-grid {
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
  } */

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
    .intech-div img{
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
      height: 70vw;
      border-radius: 1vw;
      margin-bottom: 5vw;
      padding: 3.5vw;
      gap: 25vw !important;
    }
    .eventCard {
      transform: scale(2);
      z-index: 2;
      margin-top: 10vw;
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
    
    /* .eventCard {
      width: 36vw;
      height: 40vw;
      border-radius: 24px;
      margin-top: 10vw;
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
    .eventCard .creds > h1, .eventCard .creds > a, .eventCard .creds > p {
      font-size: 2vw !important;
    } */
    /* .event-name {
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
    } */
    .button-panel {
      display: flex;
    }
    .button-panel button {
      width: 25vw;
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
    margin-bottom: 7.7vw !important;
  }

  .section {
    margin: 0 0 50px;
  }

  /* .main {
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
    align-items: start;
    width: 50vw;
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
    width: 50vw;
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
    width: 70%;
    margin: 50px auto;
  } */

  .events {
    display: flex;
    flex-wrap: wrap;
    width: fit-content;
    margin: 5vw auto;
    justify-content: center;
    gap: 4.3vw;
  }

  /* .event {
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
  } */

  /* ? RESPONSIVE ? */
  @media only screen and (max-width: 650px) {
    /* #dcbutton {
      display: none;
    } */
    .heading h1 {
      font-size: 2rem;
    }
    /* .intro {
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
    } */
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
    .events {
      gap: 60vw !important;
      margin: 33vw auto;
      /* padding: 20vw; */
    }
    .eventCard {
      transform: scale(3.6);
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
  /* @media only screen and (max-width: 450px) {
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
  } */
  /* @media only screen and (max-width: 900px) {
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
      width: 80vw;
    }
    .dclef {
      flex-direction: column;
      width: 90%;
    }
    #dchead {
      font-size: 5vh;
    }
  } */
</style>

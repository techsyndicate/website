<script>
  import { Link } from "svelte-navigator";
</script>

<svelte:head>
  <title>Tech Syndicate | Robotronics'22</title>
</svelte:head>
<div class="robo-div">
  <h1>
    Welcome to <br />
    <span>Robotronics'22</span>
  </h1>
  <p>
    Robotronics'22, the <span style="color: #16e16e;">10th edition</span> of
    Tech Syndicate's annual event, will take place from
    <span style="color: #16e16e;">October 20, 2022 to November 3, 2022</span>.
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
    <span class="link-div">
      <a href="https://ts46.club/guide" target="_blank"> Event Guide </a>
      <Link
        to="/roboEvent"
        style="text-decoration: none; color:#eee;"
        class="l"
      >
        <span class="link-span"> Events </span>
      </Link>
      <a href="https://ts46.club/register" target="_blank"> Register </a>
      <a href="/roboEvent" class="link"> Events </a>
    </span>
  </p>
  <img src="../assets/images/ts3d.png" />
</div>
<div class="video">
  <iframe
    src="https://www.youtube.com/embed/aOh8vcir49E"
    title="Robotronics'22"
    frameborder="0"
    allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
    allowfullscreen
    class="video-teaser"
  />
</div>
<div class="server-div">
  <div class="server-content">
    <h2>
      Join our <span style="color: #16e16e;">Server</span>
    </h2>
    <p>
      Join our discord server to get notified about upcoming <br />
      events. We also help and assist dipsites interested<br />
      in the fields of expertise covered by our club.
    </p>
    <br /><br />
    <a href="https://ts46.club/server"> Server Invite </a>
  </div>
  <iframe
    src="https://discord.com/widget?id=1008409770627182733&theme=dark"
    width="375"
    height="500"
    frameborder="0"
    sandbox="allow-popups allow-popups-to-escape-sandbox allow-same-origin allow-scripts"
  />
</div>
<div class="contact-div">
  <iframe
    src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3508.510822076487!2d77.06306744999999!3d28.434013899999997!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x390d1885ce7afcbf%3A0xc7f058e7154cd585!2sAMITY%20INTERNATIONAL%20SCHOOL-SECTOR%2046%2C%20Sector%2046%2C%20Gurugram%2C%20Haryana%20122022!5e0!3m2!1sen!2sin!4v1664259055057!5m2!1sen!2sin"
    width="500"
    height="350"
    style="border:0;"
    allowfullscreen=""
    loading="lazy"
    referrerpolicy="no-referrer-when-downgrade"
  />
  <div class="contact">
    <h2>
      Contact <span style="color: #16e16e;">Us</span>
    </h2>
    <br />
    <div style="margin-left: 5vw;">
      For any queries regarding Robotronics'22, you can feel free to reach out
      to us!
      <br /><br />
      <div class="contact-info">
        <ul class="contact">
          <li>
            <span
              ><span style="color: #16e16e;">Address : </span>
              Amity International School, Sector-46
              <br />
              Gurugram, Haryana 122022</span
            >
          </li>
          <li>
            <span style="margin-top: 5px;">
              <span style="color: #16e16e;">Club Email : </span> cyberamity46@gmail.com
            </span>
          </li>
          <li>
            <span>
              <span style="color: #16e16e;"
                >School Email :
              </span>aisg46@amity.edu
            </span>
          </li>
          <li />
        </ul>
      </div>
    </div>
  </div>
</div>

<style>
  .link {
    display: none;
  }
  .robo-div {
    width: 100%;
  }
  .robo-div h1 {
    font-size: 10vw;
    margin-top: 7.5vw;
  }
  .robo-div p {
    font-size: 4.5vw;
    width: 77.5vw;
  }
  .robo-div .link-div {
    display: grid;
  }
  .robo-div .link-div a,
  .robo-div .link-span {
    margin-top: 5vw;
    margin-bottom: 5vw;
    text-align: center;
    width: 65vw;
    margin-left: 1.5vw;
  }
  .robo-div img {
    transform: scale(0.6) rotate(-6deg);
    float: left;
    margin-left: -35vw;
  }
  .video {
    margin-top: -85vw !important;
    height: 50vh;
  }
  .video iframe {
    height: 75vw;
    width: 95%;
  }
  @media screen and (max-width: 768px) {
    .robo-div h1 {
      font-size: 10vw;
      margin-top: 7.5vw;
    }
    .robo-div p {
      font-size: 4.5vw;
      width: 77.5vw;
    }
    .robo-div .link-div {
      display: grid;
    }
    .robo-div .link-div a {
      margin-top: 5vw;
      margin-bottom: 5vw;
      text-align: center;
      width: 65vw;
      margin-left: 1.5vw;
    }
    .link-span {
      display: none;
    }
    .robo-div img {
      transform: scale(0.6) rotate(-6deg);
      float: left;
      margin-left: -35vw;
    }
    .video {
      margin-top: -85vw !important;
      height: 50vh;
    }
    .link {
      display: block;
    }
    .video iframe {
      height: 75vw;
      width: 95%;
    }
    .server-div {
      display: grid;
      margin-top: -5vw;
    }
    .server-div iframe {
      margin-top: 57.5vw;
      width: 90vw;
      margin-left: 2.5vw;
    }
    .server-div h2 {
      font-size: 7.5vw;
    }
    .server-div p {
      font-size: 4.5vw;
      width: fit-content;
    }
    .contact-div {
      display: grid;
      margin-top: 5vw;
    }
    .contact-div iframe {
      width: 87.5vw;
      height: 50vw;
      margin-bottom: 5vw;
    }
    .contact-div h2 {
      font-size: 7.5vw;
    }
    .contact-info {
      width: 95vw;
      margin-left: -7.5vw;
    }
  }
  .server-div iframe {
    margin-top: 57.5vw;
    width: 90vw;
    margin-left: 2.5vw;
  }
  .server-div h2 {
    font-size: 7.5vw;
  }
  .server-div p {
    font-size: 4.5vw;
    width: fit-content;
  }
  .contact-div {
    display: grid;
    margin-top: 5vw;
  }
  .contact-div iframe {
    width: 87.5vw;
    height: 50vw;
    margin-bottom: 5vw;
  }
  .contact-div h2 {
    font-size: 7.5vw;
  }
  .contact-info {
    width: 95vw;
    margin-left: -7.5vw;
  }
</style>

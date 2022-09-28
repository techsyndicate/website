<svelte:head>
    <title>Tech Syndicate | Robotronics'22</title>
</svelte:head>
<div class="robo-div">
    <h1>
        Welcome to <br />
        <span>Robotronics'22</span>
    </h1>
    <p>
        Lorem Ipsum is simply dummy text of the printing and typesetting
        industry. Lorem Ipsum has text ever since the 1500s, when an unknown
        printer took a galley of type and scrambled it to make a type specimen
        book.
        <br /><br />
        It has survived not only five centuries, but also the leap into electronic
        typesetting, remaining essentially
        <br /><br /><br /><br />
        <span class="link-div">
            <a href="" target="_blank"> Event Guide </a>
            <a href="" target="_blank"> Events </a>
            <a href="" target="_blank"> Register </a>
        </span>
    </p>
    <img src="../assets/images/snowglobe.png" />
</div>
<div class="video">
    <iframe
        src="https://www.youtube.com/embed/Zigd6oobhPg"
        title="YouTube video player"
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
        <a href=""> Server Invite </a>
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
            For any queries regarding Robotronics'22, you can feel free to reach
            out to us!
            <br /><br />
            <div class="contact-info">
                <ul class="contact">
                    <li>
                        <span
                            ><span style="color: #16e16e;">Address : </span>
                            AMITY INTERNATIONAL SCHOOL-SECTOR 46, Sector 46,
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
    .robo-div {
        width: 100%;
    }
    .robo-div h1 {
        font-size: 3.5vw;
        margin: 2.5vw 5vw;
        letter-spacing: 1.5px;
    }
    .robo-div h1 span {
        color: #16e16e;
    }
    .robo-div p {
        margin-left: 5vw;
        font-size: 1.25vw;
        letter-spacing: 1px;
        width: 35%;
    }
    .robo-div img {
        transform: scale(0.85);
        float: right;
        margin-top: -25vw;
    }
    .robo-div .link-div a {
        background: #171717;
        padding: 15px;
        margin-right: 10px;
        border-radius: 10px;
        color: #eee;
        transition: all 0.5s ease;
        text-decoration: none;
        width: 5vw;
    }
    .robo-div .link-div a:hover {
        color: #16e16e;
    }
    .server-div {
        width: 100%;
        display: flex;
        margin-top: 7.5vw;
    }
    .server-div iframe {
        border-radius: 5px;
        margin-left: 25vw;
    }
    .server-content {
        height: 25vw;
        margin-left: 5vw;
    }
    .server-content h2,
    .contact h2 {
        font-size: 3vw;
        letter-spacing: 1px;
    }
    .server-content p {
        font-size: 1.25vw;
        letter-spacing: 1px;
    }
    .server-content a {
        background: #171717;
        padding: 15px;
        margin-right: 10px;
        border-radius: 10px;
        color: #eee;
        transition: all 0.5s ease;
        text-decoration: none;
        width: 5vw;
    }
    .server-content a:hover {
        color: #16e16e;
    }
    .contact-div {
        width: 100%;
        display: flex;
        margin-top: 7.5vw;
        padding-bottom: 2.5vw;
    }
    .contact-div iframe {
        margin-left: 5vw;
        margin-top: 2.5vw;
    }
    .contact h2 {
        margin-left: 5vw;
    }
    .contact ul {
        margin-left: -2.75vw;
    }
    .contact ul li {
        margin-top: 0.5vw;
        list-style: none;
    }
    .video {
        width: 100%;
        height: 80vh;
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        margin-bottom: 12vh;
    }
    .video iframe {
        width: 80%;
        height: 100%;
        border-radius: 10px;
    }
</style>

<script>
    import {Link} from 'svelte-navigator'    
</script>
<div class="nav">
    <Link to ="/" style="text-decoration: none;">
    <div class="nav-logo"></div>
    </Link>
    <ul class="nav-links">
        <Link to = "/learn" style="text-decoration: none; color:#eee;">
            <li>
                <p>Learn</p> 
            </li>
        </Link>
        <li style="margin-top: -1.75vw;">
            |
        </li>
        <Link to = "/about" style="text-decoration: none; color:#eee;">
            <li>
                <p>About</p> 
            </li>
        </Link>
        <li style="margin-top: -1.75vw;">
            |
        </li>
        <Link to = "/event" style="text-decoration: none; color:#eee;">
            <li>
                <p>Events</p> 
            </li>
        </Link>
        <li style="margin-top: -1.75vw;">
            |
        </li>
        <Link to = "/team" style="text-decoration: none; color:#eee;">
            <li>
                <p>Team</p>
            </li>
        </Link>
        <li style="margin-top: -1.75vw;">
            |
        </li>
        <Link to = "/intech" style="text-decoration: none; color:#eee;">
            <li>
                <p>inTech</p>
            </li>
        </Link>
    </ul>
</div>
<style>
    .nav{
        width: 100%;
        display:flex;
        position: relative;
        z-index: 10;
    }
    .nav-logo{
        background: url('../assets/images/ts.png');
        background-size: cover;
        background-position: center;
        width: 4vw;
        height: 4vw;
        margin-top: 2vw;
        margin-left: 2vw;
        position: absolute;
    }
    .nav-links{
        display: flex;
        justify-content: center;
        align-items: center;
        width: 100%;
        list-style: none;
        margin-top: 3.5vw;
    }
    .nav-links li{
        display: block;
        margin: 0 1.25vw;
        font-size: 1.5vw;
        text-decoration: none;
    }
    .nav-links p{
        text-decoration: none;
        cursor: pointer;
        color: #eee;
        transition: all 0.5s ease;
        margin-top: 0vw;
    }
    .nav-links p:after{
        content : '';
        display: block;
        width: 0;
        height:2.5px;
        transition: all 0.2s ease;
        background: #16e16e;
    }
    .nav-links p:hover:after{
        width: 55%;
    }
    @media only screen and (max-width: 768px) {
        .nav{
            display: none !important;
        }
    }
</style>

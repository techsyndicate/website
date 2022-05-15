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
                <p>Learn</p> <span>|</span>
            </li>
        </Link>
        <Link to = "/about" style="text-decoration: none; color:#eee;">
            <li>
                <p>About</p> <span>|</span>
            </li>
        </Link>
        <Link to = "/event" style="text-decoration: none; color:#eee;">
            <li>
                <p>Events</p> <span>|</span>
            </li>
        </Link>
        <Link to = "/team" style="text-decoration: none; color:#eee;">
            <li>
                <p>Team</p> <span>|</span>
            </li>
        </Link>
        <Link to = "/intech" style="text-decoration: none; color:#eee;">
            <li>
                <p>Intech</p>
            </li>
        </Link>
    </ul>
</div>
<style>
    .nav{
        width: 100%;
        display:flex;
    }
    .nav-logo{
        background: url('https://raw.githubusercontent.com/techsyndicate/website/main/public/assets/images/ts.png');
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
        display: flex;
        margin: 0 1vw;
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
    .nav-links li span{
        padding-left: 1vw;
    }
    @media only screen and (max-width: 768px) {
        .nav{
            display: none !important;
        }
    }
</style>

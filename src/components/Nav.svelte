<div class="nav">
    <div class="nav-logo"></div>
    <ul class="nav-links">
        <li>
            Learn <span>|</span>
        </li>
        <li>
            Events <span>|</span>
        </li>
        <li>
            About <span>|</span>
        </li>
        <li>
            Team
        </li>
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
        margin: 0 1vw;
        font-size: 1.5vw;
        text-decoration: none;
        cursor: pointer;
    }
    .nav-links li span{
        padding-left: 1vw;
    }
</style>

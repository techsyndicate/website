<div class="nav">
    <div class="nav-logo"></div>
    <ul class="nav-links">
        <li>
          <a href="#"> Learn</a> <span>|</span>
        </li>
        <li>
           <a href="#"> Events</a> <span>|</span>
        </li>
        <li>
           <a href="#"> About</a> <span>|</span>
        </li>
        <li>
           <a href="#"> Team</a>
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
        display: flex;
        margin: 0 1vw;
        font-size: 1.5vw;
    }
    .nav-links a{
        text-decoration: none;
        cursor: pointer;
        color: #eee;
        transition: all 0.5s ease;
    }
    .nav-links a:after{
        content : '';
        display: block;
        width: 0;
        height:2.5px;
        transition: all 0.2s ease;
        background: #16e16e;
    }
    .nav-links a:hover:after{
        width: 55%;
    }
    .nav-links li span{
        padding-left: 1vw;
    }
</style>

<div class="nav-mobile">
    <Link to="/" style="text-decoration: none;"><div class="nav-logo"></div></Link>
    <button class="open">
        <i class="fa-solid fa-bars"></i>
    </button>
</div>
<div class="nav-links">
    <button class="close">
        <i class="fa-solid fa-times"></i>
    </button>
    <Link to="/" style="text-decoration: none;">
        <div class="nav-logo" style="width: 15vw; height: 15vw; display: block; margin-right: auto;margin-left: auto; margin-top: 15vw;"></div>
    </Link>
    <ul>
        <li>
            <Link to="/learn" style="text-decoration: none; color: #eee;">
                Learn
            </Link>
        </li>
        <li>
            <Link to="/event" style="text-decoration: none; color: #eee;">
                Event
            </Link>
        </li>
        <li>
            <Link to="/about" style="text-decoration: none; color: #eee;">
                About
            </Link>
        </li>
        <li>
            <Link to="/team" style="text-decoration: none; color: #eee;">
                Team
            </Link>
        </li>
        <li>
            <Link to="/intech" style="text-decoration: none; color: #eee;">
                Intech
            </Link>
        </li>
    </ul>
</div>
<script>
    import {Link} from 'svelte-navigator';
    import {onMount} from 'svelte'
    onMount(()=>{
        document.querySelector('.close').addEventListener('click',()=>{
            document.querySelector('.nav-links').style.display= 'none';
        })
        document.querySelector('.open').addEventListener('click',()=>{
            document.querySelector('.nav-links').style.display= 'block';
        })
    })
</script>
<style>
    .nav-mobile,.nav-links{
        display: none;
    }
    .nav-logo{
        background: url('../assets/images/ts.png');
        background-size: cover;
        background-position: center;
        width: 10vw;
        height: 10vw;
    }

    @media only screen and (max-width: 768px) {
        .nav-mobile{
            display: flex;
            padding-top: 5vw;
            padding-left: 2.5vw;
            padding-right:2.5vw;
        }
        .nav-mobile button,.nav-links button{
            background: #000;
            width: 10vw;
            height: 10vw;
            padding: 10px;
            border: none;
            outline:none;
            border-radius: 10px;
            transform: translateX(70vw);
        }
        .nav-links button{
            transform: translateX(80vw) translateY(5vw);
        }
        .nav-mobile i,.nav-links i{
            font-size: 5vw;
            color: #eee;
        }
        .nav-links{
            width: 100vw;
            left: 0;
            position: absolute;
            display: none;
            z-index: 150000;
            height: 125vw;
            background: #272727;
            margin-top: -16.75vw;
        }
        .nav-links ul{
            list-style: none;
            font-size: 5vw;
            text-align: center;
            margin-left: -8vw;
            margin-top: 10vw;
        }
        .nav-links li{
            margin-bottom: 5vw;
        }
    }
</style>

<ul class="nav">
    <li>
        <a href='#'>
            <div class="line line-1"></div>
        </a>
    </li>
    <li>
        <a href='#about'>
            <div class="line line-2"></div>
        </a>
    </li>
    <li>
        <a href='#events'>
            <div class="line line-3"></div>
        </a>
    </li>
    <li>
        <a href="#contact">
            <div class="line line-4"></div>
        </a>
    </li>
    <li>
        <a href="#learn">
            <div class="line line-5"></div>
        </a>
    </li>
</ul>
<nav class="mobile">
    <div></div>
    <div></div>
    <div></div>
</nav>
<div class="nav-mobile-content">
    <i class="fa-solid fa-xmark"></i>
    <ul>
        <li>
            <img src="https://github.com/techsyndicate/website/blob/main/public/assets/images/ts.png?raw=true" alt="ts-img">
        </li>
        <li>
            <a href="#">
                Home
            </a>
        </li>
        <li>
            <a href="#about">
                About
            </a>
        </li>
        <li>
            <a href="#events">
                Events
            </a>
        </li>
        <li>
            <a href="#learn">
                Resources
            </a>
        </li>
        <li>
            <a href="#contact">
                Contact
            </a>
        </li>
    </ul>
</div>
<style>
    *{
        margin: 0;
        padding: 0;
    }
    .nav{
        list-style: none;
        position: fixed;
        margin-top: 17.5vw;
        margin-left: 1vw;
        z-index: 99;
    }
    .nav li {
        width: 3.75vh;
        margin-bottom: 1vw;
    }
    .nav li .line {
        width: 100%;
        height: .35vw;
        background-color: #eee;
        transition: all 0.5s ease;
        cursor: pointer;
    }
    .nav li a{
        text-decoration: none;
    }
    .line-1::after,
    .line-2::after,
    .line-3::after,
    .line-4::after,
    .line-5::after {
        font-size: 1.5vw;
        color: #eee;
        margin-top: .5vw;
        margin-left: 1.25vw;
        position: absolute;
        display: none;
        transition: all 1s ease;
        transition-delay: 250ms; 
        transition-property: visibilty;
    }
    .line-1::after{
        content: 'Home';
    }
    .line-2::after{
        content: 'About';
    }
    .line-3::after{
        content: 'Events';
    }
    .line-4::after{
        content: 'Contact';
    }
    .line-5::after{
        content: 'Resources';
    }
    .nav li .line:hover{
        width: 150%;
        background-color: #16e16e;
        margin-bottom: 2.5vw;
    }
    .line-active{
        width: 150%;
        background-color: #16e16e;
        margin-bottom: 2.5vw;
    }
    .line-1:hover::after,
    .line-2:hover::after,
    .line-3:hover::after,
    .line-4:hover::after,
    .line-5:hover::after {
        display: block;
    }
    nav{display: none;}
    .nav-mobile-content,.nav-mobile-content ul{
        display: none;
    }
    @media screen and (max-width: 768px) {
        .nav{
            display:none;
        }
        nav{
            width: 5vh;
            height: 5vh;
            display: block;
            margin-top: -75vw;
            margin-left: 5vw;
            position: absolute;
        }
        nav div{
            width: 100%;
            height: .75vh;
            background: #eee;
            margin-bottom: 1.5vw;
        }
        .nav-mobile-content{
            background: #191919;
            width: 107.5%;
            height: 100vh;
            margin-left: -3.95%;
            margin-top: -1.65%;
        }
        .nav-mobile-content ul{
            display: block;
            margin-top: 0;
            margin-left: auto;
            text-align: center;
            list-style: none;
            font-size: 6.5vw;
            margin-top: 50%;
        }
        .nav-mobile-content ul li{
            margin-bottom: 2.5%;
        }
        .nav-mobile-content ul li a{
            color: #eee;
            text-decoration: none;
            cursor: hover;
            transition: all .5s ease;
        }
        .nav-mobile-content ul li a::before{
            content: '';
            width: 0%;
            height: .5vh;
            background: #16e16e;
            margin-bottom: 1vh;
        }
        .nav-mobile-content ul li a:hover::before{
            width: 100%;
        }
        .fa-xmark{
            font-size: 3vh;
            color: #eee;
            margin: 10% 10%;
        }
        .nav-mobile-content img{
            width: 20vh;
            margin-top: -5vh;
            margin-left: auto;
            margin-right: auto;
        }
    }
</style>
<script>
    import {onMount} from 'svelte';
    onMount(()=>{
        document.querySelector('.mobile').addEventListener('click',()=>{
            document.querySelector('.nav-mobile-content').style.display = 'block';
        })
        document.querySelector('.fa-xmark').addEventListener('click',()=>{
            document.querySelector('.nav-mobile-content').style.display = 'none';
        })
        
    })
</script>
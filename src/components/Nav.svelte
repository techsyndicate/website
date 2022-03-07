<script>
</script>
<ul>
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
        <a href="#resources">
            <div class="line line-5"></div>
        </a>
    </li>
</ul>
<style>
    *{
        margin: 0;
        padding: 0;
    }
    ul{
        list-style: none;
        position: fixed;
        margin-top: 17.5vw;
        margin-left: 1vw;
        z-index: 99;
    }
    ul li {
        width: 3.75vh;
        margin-bottom: 1vw;
    }
    ul li .line {
        width: 100%;
        height: .35vw;
        background-color: #eee;
        transition: all 0.5s ease;
        cursor: pointer;
    }
    ul li a{
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
    .line:hover{
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
</style>

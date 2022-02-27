<script>
</script>
<ul>
    <li>
        <a href='#home'>
            <div class="line"></div>
        </a>
    </li>
    <li>
        <a href='#about'>
            <div class="line"></div>
        </a>
    </li>
    <li>
        <a href='#events'>
            <div class="line"></div>
        </a>
    </li>
    <li>
        <a href="#ccc">
            <div class="line"></div>
        </a>
    </li>
    <li>
        <a href="#contact">
            <div class="line"></div>
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
    .line:hover{
        width: 120%;
        background-color: #16e16e;
    }
</style>

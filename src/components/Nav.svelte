<script>
    import Link from 'svelte-link';
    import page from 'page'
    import LandingPage from '../pages/LandingPage.svelte';
    import AboutPage from '../pages/AboutPage.svelte'
    let Home = LandingPage
    page('/',()=>(Home=LandingPage))
    page('/about',()=>(Home = AboutPage))
    page.start()
</script>
<ul>
    <li>
        <a href='/'>
            <div class="line"></div>
        </a>
    </li>
    <li>
        <a href='/about'>
            <div class="line"></div>
        </a>
    </li>
    <li>
        <a href='/events'>
            <div class="line"></div>
        </a>
    </li>
    <li>
        <Link>
            <div class="line"></div>
        </Link>
    </li>
    <li>
        <Link>
            <div class="line"></div>
        </Link>
    </li>
</ul>
<style>
    *{
        margin: 0;
        padding: 0;
    }
    ul{
        list-style: none;
        position: absolute;
        margin-top: 18.5vw;
        margin-left: 2.5vw;
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
    .line:hover{
        width: 120%;
        background-color: #16e16e;
    }
</style>
<svelte:component this={Home} />

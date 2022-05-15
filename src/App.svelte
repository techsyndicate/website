<script>
    import Nav from './components/Nav.svelte';
    import {Router, Route} from 'svelte-navigator';
    import LandingPage from './pages/LandingPage.svelte';
    import AboutPage from './pages/AboutPage.svelte';
    import MemberPage from './pages/MemberPage.svelte';
    import EventPage from './pages/EventPage.svelte';
    import LearnPage from './pages/LearnPage.svelte';
    import IntechPage from './pages/IntechPage.svelte';
    import MobileNav from './components/MobileNav.svelte';
</script>
<Router>
    <MobileNav />
    <Nav />
    <Route path="learn" component={LearnPage}/>
    <Route path="about" component={AboutPage}/>
    <Route path="team" component={MemberPage}/>
    <Route path="event" component={EventPage}/>
    <Route path="intech" component={IntechPage}/>
    <Route path="/" component={LandingPage} />
</Router>
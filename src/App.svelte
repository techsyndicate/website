<script>
  import Nav from "./components/Nav.svelte";
  import { Router, Route, navigate } from "svelte-navigator";
  import LandingPage from "./pages/LandingPage.svelte";
  import AboutPage from "./pages/AboutPage.svelte";
  import MemberPage from "./pages/MemberPage.svelte";
  import EventPage from "./pages/EventPage.svelte";
  import LearnPage from "./pages/LearnPage.svelte";
  import MobileNav from "./components/MobileNav.svelte";
  import Tbr from "./pages/TBR.svelte";
  import Robotronics from "./pages/Robotronics.svelte";
  import Registration from "./pages/Registration.svelte";
</script>

<Router>
  <MobileNav />
  <Nav />
  <Route path="learn" component={LearnPage} />
  <Route path="about" component={AboutPage} />
  <!-- <Route path="intech" component={TgPage} /> -->
  <Route path="/" component={LandingPage} />
  <Route path="event" component={EventPage} />
  <Route path="/tbr" component={Tbr} />
  <Route path="tg" component={Robotronics} />
  <Route path="team" component={MemberPage} />
  <Route path="register" component={Registration} />
</Router>

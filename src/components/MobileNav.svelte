<body>
    <nav>
      <div class="navbar">
        <div class="container nav-container">
          <input class="checkbox" type="checkbox" name="" id="" />
            <div class="hamburger-lines">
              <span class="line line1"></span>
              <span class="line line2"></span>
              <span class="line line3"></span>
            </div>  
          <div class="logo">
            <a href="/"><img src="/assets/images/ts.png" alt="dare - go touch grass" width="45" height="45"></a>
          </div>
          <div class="menu-items" id="menu">
            <li><a href="/"><img src="/assets/images/ts.png" alt="dare - go touch grass" width="45" height="45"></a></li>
            <li><a href="/learn" class='link'>Learn</a></li>
            <li><a href="/event" class='link'>Events</a></li>
            <li><a href="/about" class='link'>About</a></li>
            <li><a href="/team" class='link'>Team</a></li>
            <!-- <li><a href="/robo" class='link'>Robotronics</a></li> -->
            <li><a href="/tg" class='link'>Training Grounds</a></li>
          </div>
        </div>
      </div>
    </nav>
  </body>

<style>
 @import url("https://fonts.googleapis.com/css2?family=Poppins:ital,wght@0,100;0,200;0,300;0,400;0,500;0,600;0,700;0,800;0,900;1,100;1,200;1,300;1,400;1,500;1,600;1,700;1,800;1,900&display=swap");

 
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body {
  font-family: "Poppins", sans-serif;
}

.container {
  max-width: 1050px;
  width: 90%;
  margin: auto;
}

.navbar {
  width: 100%;
  padding-top: 1vh;
}

.nav-container {
  display: flex;
  justify-content: space-between;
  align-items: center;
  height: 62px;
}

.navbar .menu-items {
  display: flex;
}

.navbar .nav-container li {
  list-style: none;
}

.navbar .nav-container a {
  text-decoration: none;
  color: #fff;
  font-weight: 500;
  font-size: 1.2rem;
  padding: 0.7rem;
}

.navbar .nav-container .link {
  text-decoration: none;
  color: #fff;
  font-weight: 500;
  font-size: 1.2rem;
  padding: 0.7rem;
}

.link{
  text-decoration: none;
  color: #fff;
  font-weight: 500;
  font-size: 1.2rem;
  padding: 0.7rem;
}

.navbar .nav-container a:hover{
    font-weight: bolder;
}

.nav-container {
  display: block;
  position: relative;
  height: 60px;
}

.nav-container .checkbox {
    position: absolute;
    display: block;
    height: 19.5px;
    width: 24px;
    top: 20px;
    right: 10px;
    z-index: 102;
    opacity: 0;
    cursor: pointer;
}

.nav-container .hamburger-lines {
  display: block;
  height: 19.5px;
  width: 24px;
  position: absolute;
  top: 17px;
  right: 10px;
  z-index: 101;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
}

.nav-container .hamburger-lines .line {
  display: block;
  height: 2px;
  width: 100%;
  border-radius: 10px;
  background: #fff;
}

.nav-container .hamburger-lines .line1 {
  transform-origin: 0% 100%;
  transition: transform 0.4s ease-in-out;
}

.nav-container .hamburger-lines .line2 {
  transition: transform 0.2s ease-in-out;
}

.nav-container .hamburger-lines .line3 {
  transform-origin: 0% 0%;
  transition: transform 0.4s ease-in-out;
}

.navbar .menu-items {
  padding-top: 120px;
  background-color: #272727f7;
  height: 110vh;
  width: 110%;
  transform: translate(-150%);
  display: flex;
  flex-direction: column;
  margin-left: -40px;
  padding-left: 15px;
  transition: transform 0.5s ease-in-out;
  text-align: center;
      position: fixed;
    z-index: 100;
    margin-top: -20px;
}

.navbar .menu-items li {
  margin-bottom: 1.2rem;
  font-size: 1.5rem;
  font-weight: 500;
}

.logo {
  position: absolute;
  top: 5px;
  left: -10px;
  font-size: 1.2rem;
}

.nav-container input[type="checkbox"]:checked ~ .menu-items {
  transform: translateX(0);
}

.nav-container input[type="checkbox"]:checked ~ .hamburger-lines .line1 {
  transform: rotate(45deg);
}

.nav-container input[type="checkbox"]:checked ~ .hamburger-lines .line2 {
  transform: scaleY(0);
}

.nav-container input[type="checkbox"]:checked ~ .hamburger-lines .line3 {
  transform: rotate(-45deg);
}

.nav-container input[type="checkbox"]:checked ~ .logo{
  display: none;
}

@media screen and (min-width: 750px) and (max-width: 8000px) {
    .navbar {
  display: none;
}}

</style>

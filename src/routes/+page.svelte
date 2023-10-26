<script lang="ts">
  import { base } from '$app/paths';
</script>

<head>
  <meta charset="UTF-8" />
  <meta http-equiv="X-UA-Compatible" content="IE=edge" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Crystal Client</title>
</head>

<body>
  <nav class="navbar">
    <div class="logo">
        <img src="src/assets/crystal.png" alt="logo"/>
    </div>

    <ul class="nav-links">
      <div class="menu">

        <li><a href="{base}/">Home</a></li>
        <li><a href="{base}/">Installation</a></li>
        <li><a href="{base}/">FAQ</a></li>
        <li><a href="{base}/">Login</a></li>
      </div>
    </ul>
  </nav>

  <div class="banner">
    <h1>Crystal Client</h1>
    <p class="fab">The first and best <color>Cross Platform</color> mod menu for Geometry Dash</p>
    <a href="https://github.com/ninXout/Crystal-Client/releases/download/v4.0.1/ninxout.crystalclient.geode"><button class="btn" data="Download Crystal v4.0.1"></button></a>
    <a href="https://github.com/ninXout/Crystal-Client"><button style="transform:translate(-405px, 80px)" class="btn" data="View repository on GitHub"></button> </a>
    <img src="src/assets/modmenu.png" alt="modmenu" />
  </div>

  <div class="showcase">
    <button class="btn" data="Download Crystal v4.0.1"></button>
  </div>
</body>

<style>
::-webkit-scrollbar {
    display: none;
}

@font-face {
    font-family: ModernSans;
    src: url("/assets/CeraPro.otf");
}

* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body {
    font-family: ModernSans;
    font-weight: bold;
    background-image: linear-gradient(to bottom, #191624, #2d2a47);
    background-attachment: fixed;
    background-size: cover;
    overflow-x:hidden;
    scrollbar-width: none;
    -ms-overflow-style: none;
}

a {
  text-decoration: none;
}

li {
  list-style: none;
}

.navbar {
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding: 10px;
  background-color: rgba(255,255,255,0.03);
    backdrop-filter: blur(5px);
    -webkit-backdrop-filter: blur(5px);
  color: #fff;
    z-index: 99;
}

.nav-links a {
  color: #fff;
}

.logo {
  font-size: 22px;
}

.logo img {
    height: 50px;
    transition: 0.2s;
    float: left;
}

.logo img:hover {
    filter: brightness(130%);
}

.logo h1 {
    position: relative;
    width: 150%;
    margin-top: 12px;
    left: 15px;
}

.menu {
  display: flex;
  gap: 1em;
  font-size: 18px;
}

.menu li:hover {
  background-color: rgba(72, 119, 147, 0.1);
  filter: contrast(0%) brightness(200%);
  border-radius: 8px;
  transition: 0.3s ease;
}

.menu li {
  padding: 10px 19px;
}

.banner h1 {
    margin: 0;
    padding: 10vw 0 0 8vh;
    font-size: 400%;
    color: white;
    z-index: 3;
}

.banner p {
    font-family: ModernSans;
    margin: 0;
    padding: 1vw 0 0 8vh;
    font-size: 150%;
    color: white;
    z-index: 3;
    width: 38%;
}

.banner img {
    width: 62vw;
    transform: translate(510px, -300px);
    right: 0.5vw;
    bottom: 8vh;
    border-radius: 3vw;
    pointer-events: none;
}

.glow {
    -webkit-animation: glow 1s ease-in-out infinite alternate;
  -moz-animation: glow 1s ease-in-out infinite alternate;
  animation: glow 1s ease-in-out infinite alternate;
}

@-webkit-keyframes glow {
  from {
    text-shadow: 0 0 15px #00ffa3, 0 0 15px #dc1fff;
  }
  to {
    text-shadow: 0 0 15px #00ffa3, 0 0 15px #dc1fff;
  }
}

.banner color {
    background-image: linear-gradient(to left, #6c1fff, #dc1fff);
    background-clip: text;
    background-size: 110%;
    background-position: left;
    background-repeat: no-repeat;
    -webkit-background-clip: text;
    color: transparent;
    animation: b1c 2s ease-in-out normal;
}

.btn {
  padding: 20px 60px;
  margin-left: 50px;
  margin-top: 20px;
  width: 50vh;
  border: none;
  outline: none;
  position: relative;
  z-index: 1;
  border-radius: 10px;
  background: linear-gradient(to right, #ff1fb2, #e241fe);
  cursor: pointer;
    transition: 0.3s;
}

.btn::before {
  content: "";
  position: absolute;
  left: 1px;
  right: 1px;
  top: 1px;
  bottom: 1px;
  border-radius: 9px;
  background-color: rgba(0,0,0,1);
  z-index: -1;
  transition: 200ms;
}

.btn::after {
  content: attr(data);
  font-size: 16px;
  background: linear-gradient(to left, #ff1fb2, #dc1fff);
  -webkit-background-clip: text;
  color: transparent;
  transition: 200ms;
}

.btn:hover::before {
  opacity: 50%;
  top: 0px;
  right: 0px;
  bottom: 0px;
  left: 0px;
}

.btn:hover::after {
  color: black;
  background-position: center;
}

.showcase {
    transform: translateY(200px);
    padding: 350px 0 0 0;
    margin: 0;
    backdrop-filter: blur(8px);
}

</style>
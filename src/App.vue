<template>
  <div id="app">
    <!-- <div id="nav">
      <div class="nav-logo">
        <router-link to="/">LOGO</router-link>
      </div>
      <div class="nav-links">
        <router-link to="/">Home</router-link>
        <router-link to="/skills">Skills</router-link>
        <router-link to="/gallery">Gallery</router-link>
        <router-link to="/about">About</router-link>
      </div>
    </div>-->

    <nav class="navbar navbar-expand-lg navbar-light bg-transparent pt-4">
      <router-link to="/"><img class="logo" src="../public/Logo01.png" alt="Logo"></router-link>
      <button
        class="navbar-toggler"
        type="button"
        data-toggle="collapse"
        data-target="#navbarSupportedContent"
        aria-controls="navbarSupportedContent"
        aria-expanded="false"
        aria-label="Toggle navigation"
      >
        <span class="navbar-toggler-icon"></span>
      </button>

      <div class="collapse navbar-collapse pr-4" id="navbarSupportedContent">
        <ul class="navbar-nav ml-auto">
          <li class="nav-item mx-2 hvr-underline-from-center">
            <router-link to="/">Home</router-link>
          </li>
          <li class="nav-item mx-2 hvr-underline-from-center">
            <router-link to="/skills">Skills</router-link>
          </li>
          <li class="nav-item mx-2 hvr-underline-from-center">
            <router-link to="/projects">Projects</router-link>
          </li>
          <li class="nav-item mx-2 hvr-underline-from-center">
            <router-link to="/about">About</router-link>
          </li>
        </ul>
      </div>
    </nav>
    <transition
      name="router-anim"
      enter-active-class="animated fadeIn"
      leave-active-class="animated fadeOut"
    >
      <router-view />
    </transition>
  </div>
</template>

<style>

/* Nav-Link underline animation */

.hvr-underline-from-center {
  display: inline-block;
  vertical-align: middle;
  -webkit-transform: translateZ(0);
  transform: translateZ(0);
  box-shadow: 0 0 1px rgba(0, 0, 0, 0);
  -webkit-backface-visibility: hidden;
  backface-visibility: hidden;
  -moz-osx-font-smoothing: grayscale;
  position: relative;
  overflow: hidden;
}
.hvr-underline-from-center:before {
  content: "";
  position: absolute;
  z-index: -1;
  left: 50%;
  right: 50%;
  bottom: 0;
  background: #2b70dc;
  height: 4px;
  -webkit-transition-property: left, right;
  transition-property: left, right;
  -webkit-transition-duration: 0.3s;
  transition-duration: 0.3s;
  -webkit-transition-timing-function: ease-out;
  transition-timing-function: ease-out;
}
.hvr-underline-from-center:hover:before, .hvr-underline-from-center:focus:before, .hvr-underline-from-center:active:before {
  left: 0;
  right: 0;
}

/* #app {
  font-family: "Raleway", sans-serif;
} */

@import "https://cdnjs.cloudflare.com/ajax/libs/animate.css/3.7.2/animate.min.css";

nav {
  font-family: "Montserrat", sans-serif;
  font-weight: 600;
  font-size: 1.2em;
  margin-bottom: 30px;
}

nav a {
  /* color: #434655; */
  color: #000;
  margin: 0 10px;
  text-decoration: none;
  /* transition: 0.5s ease all; */
}

nav a:hover {
  text-decoration: none;
  /* font-size: 1.3em; */
}

nav a.router-link-exact-active {
  color: #2b70dc;
}

.logo {
  width: 70px;
  height: auto;
}

::-moz-selection { /* Code for Firefox */
  color: #000;
  background: rgba(0,0,0,0.1);
}

::selection {
  color: #000;
  background: rgba(0,0,0,0.1);
}

/* .page {
  position: fixed;
} */
</style>

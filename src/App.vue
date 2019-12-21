<template>
  <div id="app">
    <!-- <nav class="navbar navbar-expand-lg navbar-light bg-transparent pt-4">
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
          <li class="nav-item mx-2">
            <router-link to="/">Home</router-link>
          </li>
          <li class="nav-item mx-2">
            <router-link to="/skills">Skills</router-link>
          </li>
          <li class="nav-item mx-2">
            <router-link to="/projects">Projects</router-link>
          </li>
          <li class="nav-item mx-2">
            <router-link to="/about">About</router-link>
          </li>
        </ul>
      </div>
    </nav>-->

    <nav class="navbar">
      <div class="logo">
        <router-link to="/">
          <img class="logo" src="../public/Logo01.png" alt="Logo" />
        </router-link>
      </div>
      <ul class="nav-links">
        <li class="nav-item">
          <router-link to="/">Home</router-link>
        </li>
        <li class="nav-item">
          <router-link to="/skills">Skills</router-link>
        </li>
        <li class="nav-item">
          <router-link to="/projects">Projects</router-link>
        </li>
        <li class="nav-item">
          <router-link to="/about">About</router-link>
        </li>
      </ul>

      <div class="hamburger">
        <div class="line one"></div>
        <div class="line"></div>
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


<script>
window.addEventListener("load", function() {
  var hamburger = document.querySelector(".hamburger");
  hamburger.addEventListener("click", () => {
    hamburger.classList.toggle("open1");
    const navLinks = document.querySelector(".nav-links");
    const links = document.querySelectorAll(".nav-links li");
    navLinks.classList.toggle("open");
    // line.classList.toggle("open1");
    links.forEach(link => {
      link.addEventListener("click", () => {
        navLinks.classList.remove("open");
        hamburger.classList.remove("open1");
      });
    });
  });
});

export default {
  name: "Home"
};
</script>


<style>
#app {
  font-family: "Montserrat", sans-serif;
}

body {
  /* font-family: "Raleway", sans-serif; */
  margin: 0;
  padding: 0;
}

ul {
  padding: 0;
  margin: 0;
}

@import "https://cdnjs.cloudflare.com/ajax/libs/animate.css/3.7.2/animate.min.css";

.navbar {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 0;
  font-family: "Montserrat", sans-serif;
  font-weight: 600;
  font-size: 1.2em;
  margin-bottom: 30px;
  height: 15vh;
}

.logo {
  margin-left: 15px;
  width: 65px;
  height: 65px;
}

.logo img {
  width: 100%;
  height: 100%;
}

.nav-links {
  display: flex;
  justify-content: space-around;
  margin-right: 30px;
  width: 30%;
}

.nav-links a {
  text-decoration: none;
  color: rgb(73, 80, 87);
}

.nav-links a:hover {
  color: #2b70dc;
}

.nav-links li {
  list-style: none;
}

nav a.router-link-exact-active {
  color: #2b70dc;
}

.hamburger {
  display: none;
}

@media only screen and (max-width: 1200px) {
  .nav-links {
    width: 50%;
  }
}

@media only screen and (max-width: 768px) {
  .navbar {
    position: relative;
    width: 80%;
    margin: auto;
  }

  .logo {
    margin-left: -8px;
  }

  .hamburger {
    display: block;
    /* margin-right: 30px; */
    position: absolute;
    right: 0;
    top: 7.5vh;
    transform: translateY(-50%);
    cursor: pointer;
    z-index: 2;
  }

  .line {
    width: 25px;
    height: 2.5px;
    background: #000;
    margin: 6px;
    transition: all 0.3s ease-in-out;
  }

  .line.one {
    width: 20px;
  }
/* 
  .line.two {
    transform: rotate(-45deg);
  } */

  .hamburger.open1 {
    position: fixed;
    right: 10%;
  }

  .nav-links {
    position: fixed;
    background: #2b70dc;
    /* background-image: url('./assets/hamburger_menu.jpg'); */
    background-image: linear-gradient(
        to bottom,
        rgba(255, 255, 255, 0.52),
        rgba(43, 112, 220, 1)
      ),
      url("./assets/hamburger_menu1.jpg");
    background-size: cover;
    /* opacity: 0.3; */
    right: 0px;
    height: 100vh;
    width: 100%;
    margin: 0;
    bottom: 0;
    justify-content: center;
    align-items: center;
    flex-direction: column;
    clip-path: circle(100px at 90% -18%);
    -webkit-clip-path: circle(100px at 90% -18%);
    transition: all 1s ease-in-out;
    pointer-events: none;
    z-index: 2;
  }

  .nav-links li {
    padding: 30px 0;
  }

  .nav-links a {
    color: #fff;
    transition: all 0.2s cubic-bezier(0.075, 0.82, 0.165, 1);
  }

  nav a.router-link-exact-active {
    background: #fff;
    color: #2b70dc;
    padding: 10px 15px;
    border-radius: 10px;
  }

  .nav-links a:hover {
    background: #fff;
    color: #2b70dc;
    padding: 10px;
    border-radius: 10px;
  }

  .nav-links.open {
    clip-path: circle(1392px at 90% -18%);
    -webkit-clip-path: circle(1392px at 90% -18%);
    pointer-events: all;
  }
}

::-moz-selection {
  /* Code for Firefox */
  color: #000;
  background: rgba(0, 0, 0, 0.1);
}

::selection {
  color: #000;
  background: rgba(0, 0, 0, 0.1);
}

/* ScrollBar styles */
/* width */
::-webkit-scrollbar {
  width: 8px;
}

/* Track */
::-webkit-scrollbar-track {
  background: #e2e2e2;
}

/* Handle */
::-webkit-scrollbar-thumb {
  background: #888;
  border-radius: 20px;
}

/* Handle on hover */
::-webkit-scrollbar-thumb:hover {
  background: #555;
}
</style>

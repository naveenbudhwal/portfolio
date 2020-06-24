<template>
  <div>
    <nav class="navbar">
      <div class="logo">
        <router-link to="/">
          <img class="logo" src="../../public/Logo01.png" alt="Logo" />
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

      <div @click="switchToDark" class="dark-mode-btn">
        <span><img src="../assets/light.svg" alt=""></span>
        <label class="switch">
          <input type="checkbox">
          <div>
            <span></span>
          </div>
        </label>
        <span><img src="../assets/dark.svg" alt=""></span>
      </div>
      
      <div id="nav-icon1">
        <span></span>
        <span></span>
        <span></span>
      </div>

    </nav>
  </div>
</template>

<script>
  window.addEventListener("load", function() {
  const navLinks = document.querySelector(".nav-links");
  const navIcon = document.querySelector("#nav-icon1");
  const links = document.querySelectorAll(".nav-links li");
  navIcon.addEventListener("click", function() {
    navLinks.classList.toggle("open");
    navIcon.classList.toggle("open2");
    navIcon.classList.toggle("fix");
    links.forEach(link => {
      link.addEventListener("click", () => {
        navLinks.classList.remove("open");
        navIcon.classList.remove("open2");
        navIcon.classList.remove("fix");
      });
    });  
  })
});

export default {
  name: 'Home',
  methods: {
    switchToDark () {
      this.$store.commit('TOGGLE_DARK_MODE')
    }
  }
}
</script>

<style scoped>

.switch {
  cursor: pointer;
}

.switch input {
  display: none;
}

.switch input + div {
  position: relative;
}

.switch input + div:before,
.switch input + div:after {
  --s: 1;
  content: '';
  position: absolute;
  height: 4px;
  top: 10px;
  width: 24px;
  background: #505162;
  transform: scaleX(var(--s));
  transition: transform .3s ease;
}

.switch input + div:before {
  --s: 0;
  left: 0;
  transform-origin: 0 50%;
  border-radius: 2px 0 0 2px;
}
.switch input + div:after {
  left: 28px;
  transform-origin: 100% 50%;
  border-radius: 0 2px 2px 0;
}

.switch input + div span {
  padding-left: 56px;
  line-height: 24px;
  color: #9EA0BE;
}

.switch input + div span:before {
  --x: 0;
  --b: #9EA0BE;
  --s: 4px;
  content: '';
  position: absolute;
  left: 0;
  top: 0;
  width: 24px;
  height: 24px;
  border-radius: 50%;
  box-shadow: inset 0 0 0 var(--s) var(--b); 
  transform: translateX(var(--x));
  transition: box-shadow .3s ease, transform .3s ease;
}

.switch input + div span:not(:empty) {
  padding-left: 64px;
}

input:checked + div:before {
  --s: 1;
}
input:checked + div:after {
  --s: 0;
}

input:checked + div span:before {
  --x: 28px;
  --s: 12px;
  --b: #F7F8FF;
}

#nav-icon1 {
  display: none;
  width: 35px;
  height: 35px;
  -webkit-transform: rotate(0deg);
  -moz-transform: rotate(0deg);
  -o-transform: rotate(0deg);
  transform: rotate(0deg);
  -webkit-transition: .5s ease-in-out;
  -moz-transition: .5s ease-in-out;
  -o-transition: .5s ease-in-out;
  transition: .5s ease-in-out;
  cursor: pointer;
  z-index: 2;
}

#nav-icon1 span {
  display: block;
  position: absolute;
  height: 5px;
  width: 100%;
  background: #434655;
  border-radius: 9px;
  opacity: 1;
  left: 0;
  -webkit-transform: rotate(0deg);
  -moz-transform: rotate(0deg);
  -o-transform: rotate(0deg);
  transform: rotate(0deg);
  -webkit-transition: .25s ease-in-out;
  -moz-transition: .25s ease-in-out;
  -o-transition: .25s ease-in-out;
  transition: .25s ease-in-out;
}

#nav-icon1 span:nth-child(1) {
  opacity: 0;
  top: 5px;
}

#nav-icon1 span:nth-child(2) {
  width: 28px;
  top: 15px;
}

#nav-icon1 span:nth-child(3) {
  top: 25px;
}

#nav-icon1.open2 span:nth-child(1) {
  opacity: 1;
  top: 18px;
  -webkit-transform: rotate(135deg);
  -moz-transform: rotate(135deg);
  -o-transform: rotate(135deg);
  transform: rotate(135deg);
}

#nav-icon1.open2 span:nth-child(2) {
  opacity: 0;
  left: -60px;
}

#nav-icon1.open2 span:nth-child(3) {
  top: 18px;
  -webkit-transform: rotate(-135deg);
  -moz-transform: rotate(-135deg);
  -o-transform: rotate(-135deg);
  transform: rotate(-135deg);
}

#nav-icon1.fix {
  position: fixed;
  right: 10%;
}

.navbar {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 0 0.8em;
  font-weight: 600;
  font-size: 1.2em;
  height: 15vh;
}

.logo {
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
  align-items: center;
  /* width: 30%; */
}

.dark-mode-btn {
  display: flex;
  justify-content: center;
  align-items: center;
}

.dark-mode-btn span img {
  width: 20px;
  height: auto;
}

.nav-item {
  margin: 0 1em;
  list-style: none;
}

.nav-item a {
  text-decoration: none;
  color: #939393;
  letter-spacing: 0.04em;
  transition: all 140ms cubic-bezier(.55,.06,.68,.19);
}

.nav-item a:hover {
  color: #000;
}

nav a.router-link-exact-active {
  color: #000;
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

  #nav-icon1 {
    display: block;
  }

  .logo {
    margin-left: -8px;
  }

  .nav-links {
    position: fixed;
    background: #2b70dc;
    transform: translateX(100vh);
    right: 0px;
    height: 100vh;
    width: 60%;
    margin: 0;
    bottom: 0;
    justify-content: center;
    align-items: center;
    flex-direction: column;
    transition: all 0.8s ease-in-out;
    pointer-events: none;
    z-index: 2;
  }

  .nav-item {
    padding: 1.5em 0;
  }

  .nav-item a {
    color: #fff;
    transition: all 0.2s cubic-bezier(0.075, 0.82, 0.165, 1);
  }

  nav .nav-links a.router-link-exact-active {
    color: #fff;
    position: relative;
  }

  nav .nav-item a.router-link-exact-active::before {
    content: ''; 
    position: absolute;
    width: 2.8em;
    height: 0.5em;
    background: rgb(41, 41, 41);
    bottom: 0;
    left: 0;
    z-index: -1;
  }

  .nav-item a:hover {
    color: #434655;
    font-size: 1.2em;
  }

  .nav-links.open {
    transform: translateX(0);
    pointer-events: all;
  }
}

</style>
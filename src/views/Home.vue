<template>
  <div class="root">
    <div class="wrapper">
      <div class="main">
        <div class="first-half">
          <div class="intro">
            <p>
              Hi<span class="color">,</span> I<span class="color">'</span>m
            </p>
            <p>
              <span class="bold">Naveen</span>
              <span class="color bold">.</span>
            </p>
          </div>
          <hr class="material-hr" />
          <div class="sub-intro">
            <p>Web Developer</p>
            <!-- <p>Tech Enthusiast</p> -->
          </div>
        </div>
        <div class="second-half">
          <div class="avatar">
            <img src="../assets/portrait.png" alt="My photo" />
          </div>
        </div>
      </div>
    </div>
    <SocialNav class="bottom" />
  </div>
</template>

<script>

import SocialNav from '@/components/SocialNav.vue';

export default {
  name: "home",
  components: {
    SocialNav
  }
};
</script>

<style scoped>

.root {
  height: 85vh;
}

.main {
  display: flex;
  justify-content: space-around;
  padding-bottom: 10px;
}

.first-half {
  width: 40%;
}
.second-half {
  width: 40%;
}

.intro {
  text-align: start;
  font-weight: 400;
  font-size: 4rem;
  color: #434655;
  padding-top: 5%;
  padding-left: 20%;
}

.intro p {
  margin: 30px 0;
}

.avatar {
  padding-right: 100px;
  animation: float 5s ease-in-out infinite;
}

@keyframes float {
  0% {
    transform: translatey(0px);
  }
  50% {
    transform: translatey(-30px);
  }
  100% {
    transform: translatey(0px);
  }
}

.avatar img {
  width: 25rem;
  height: auto;
}

.cursor {
  font-size: 0.9em;
}

.sub-intro {
  text-align: start;
  font-weight: 700;
  font-size: 2rem;
  color: #2b70dc;
  padding-left: 20%;
  margin-bottom: 0px;
}

.material-hr {
  width: 100px;
  border: 0;
  height: 7px;
  background: #2b70dc;
  border-radius: 7px;
  margin-left: 20%;
  /* margin-bottom: 10%; */
}

i {
  color: #2b70dc;
}

/* ::-moz-selection {
  color: #fff;
  background: #000;
}

::selection {
  color: #fff;
  background: #000;
} */

.color {
  color: #2b70dc;
}

.color2 {
  color: #76a5ff;
}

.bold {
  font-weight: 600;
}

.bottom {
  position: absolute;
  bottom: 1em;
  left: 50%;
  transform: translateX(-50%);
}

@media only screen and (max-width: 1200px) {
  .main {
    flex-direction: column;
  }
  .first-half {
    order: 2;
    width: 100%;
  }
  .second-half {
    order: 1;
    width: 100%;
  }
  .avatar {
    animation: none;
    text-align: center;
    padding-right: 0;
  }
  .avatar img {
    width: 20rem;
    height: auto;
  }
  .intro {
    padding-left: 0;
    text-align: center;
    font-size: 4rem;
  }
  .sub-intro {
    padding-left: 0;
    text-align: center;
    font-size: 1.8rem;
    margin-top: 20px;
  }
  .material-hr {
    margin: 0 auto;
  }
  .social-media-bar a {
    margin: 0 10px;
  }
}

@media only screen and (max-width: 760px) {
  .avatar img {
    width: 17rem;
    height: auto;
  }
  .intro {
    font-size: 3.5rem;
  }
  .sub-intro {
    font-size: 1.6rem;
  }
  .social-media-bar a {
    margin: 0 10px;
  }
}

@media only screen and (max-width: 350px) {
  .social-media-bar a {
    margin: 0 5px;
  }
}
</style>
<template>
  <div class="root">
    <div class="wrapper">
      <div class="main">
        <div class="first-half">
          <div class="intro">
            <p>Hi<span class="color">,</span> I<span class="color">'</span>m </p>
            <p><span class="bold">Naveen</span><span class="color bold">.</span></p>
          </div>
          <hr class="material-hr">
          <div class="sub-intro">
            <p>Web Developer</p>
            <p>Coder</p>
          </div>
        </div>
        <div class="second-half">
          <div class="avatar">
            <img src="../assets/portrait.png" alt="My photo">
          </div>
        </div>
      </div>
    </div>

    <div class="social-media-bar">
      <a href="mailto:naveenbudhwal@gmail.com" target="_blank" rel="noopener">
          <i class="far fa-envelope"></i>
      </a>
      <a href="https://www.instagram.com/naveenbudhwal" target="_blank" rel="noopener">
        <i class="fab fa-instagram"></i>
      </a>
      <a href="https://www.linkedin.com/in/naveenbudhwal" target="_blank" rel="noopener">
        <i class="fab fa-linkedin-in"></i>
      </a>
      <a href="https://www.github.com/naveenbudhwal" target="_blank" rel="noopener">
        <i class="fab fa-github"></i>
      </a>
      <a href="https://www.twitter.com/naveenbudhwal" target="_blank" rel="noopener">
        <i class="fab fa-twitter"></i>
      </a>
    </div>

  </div>
  
</template>

<script>

// var cursor = true;
// var speed = 500;

// setInterval(() => {
//    if(cursor) {
//      document.querySelector('.cursor').style.opacity = 0;
//      cursor = false;
//    } else {
//      document.querySelector('.cursor').style.opacity = 1;
//      cursor = true;
//    }
// }, speed);

export default {
  name: "home"
};
</script>

<style scoped>

/* .wrapper {
  min-height: 100%;
} */

.main {
  display: flex;
  justify-content: space-around;
  padding-bottom: 50px;
}

.intro {
  text-align: start;
  font-family: "Montserrat", sans-serif;
  font-weight: 400;
  font-size: 5rem;
  color: #434655;
  padding-top: 5%;
  padding-left: 20%; 
}

.avatar {
  padding-right: 100px;
	/* transform: translatey(0px); */
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
  font-family: "Montserrat", sans-serif;
  font-weight: 600;
  font-size: 2rem;
  color: #76A5FF;
  padding-left: 20%;
  /* margin-top: 50px; */
}

.material-hr {
  width: 100px;
  border: 0;
  height: 7px;
  background: #2b70dc;
  border-radius: 7px;
  margin-left: 20%;
  margin-bottom: 10%;
}

i {
  color: #2b70dc;
}

.social-media-bar {
  position: relative;
  height: 50px;
  margin-bottom: 20px;
  text-align: center;
}

.social-media-bar a {
  font-size: 20px;
  text-align: center;
  margin: 0 20px;
}

.social-media-bar a i {
  /* padding: 16px; */
  padding: 10px;
  border: 2px solid #AED6FF;
  border-radius: 100%;
  font-size: 22px;
  width: 48px;
  height: 48px;
  transition: all 0.3s ease;
}

.social-media-bar a i:hover {
  color: #fff;
  background: #2b70dc;  
  border: 2px solid #AED6FF;
}

/* .fa-twitter {
  background: #1DA1F2;
  color: #fff;
}

.fa-linkedin-in {
  background: #2867B2;
  color: #fff;
}

.fa-envelope {
  background: #DB4437;
  color: #fff;
}

.fa-instagram {
  background: #C13584;
  color: #fff;
}

.fa-github {
  background: #000;
  color: #fff;
} */

::-moz-selection { /* Code for Firefox */
  color: #fff;
  background: #000;
}

::selection {
  color: #fff;
  background: #000;
}

.color {
  color: #2b70dc;
}

.color2 {
  color: #76A5FF;
}

.bold {
  font-weight: 600;
}

@media only screen and (max-width: 1200px) {
  .main {
    flex-direction: column;
  }
  .first-half {
    order: 2;
  }
  .second-half {
    order: 1;
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
    /* display: flex;
    justify-content: center; */
  }
  .material-hr {
    margin: 0 auto;
  }
  .social-media-bar a {
    margin: 0 10px;
  }
}

</style>
<template>
  <div class="root">
    <div class="main">
      <div class="first-half">
        <div class="intro">
          Hi <span class="color">,</span> 
          <p>I<span class="color">'</span>m <span class="bold">Naveen</span>  <span class="color cursor">|</span></p>
        </div>
        <div class="sub-intro">Web Developer <span class="color bold">|</span>  Coder
        </div>
      </div>
      <div class="second-half">
        <div class="avatar">
          <img src="../assets/portrait.png" alt="My photo">
        </div>
      </div>
    </div>

    <!-- <div class="footer">
      <a href="mailto:naveenbudhwal@gmail.com">
          <span class="icon">
            <i class="far fa-envelope"></i>
          </span>
      </a>
      <a href="#">
        <span class="icon">
          <i class="fab fa-instagram"></i>
        </span>
      </a>
      <a href="#">
        <span class="icon">
          <i class="fab fa-linkedin-in"></i>
        </span>
      </a>
      <a href="#">
        <span class="icon">
          <i class="fab fa-github"></i>
        </span>
      </a>
      <a href="#">
        <span class="icon">
          <i class="fab fa-twitter"></i>
        </span>
      </a>
    </div> -->

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

.main {
  display: flex;
  justify-content: space-around;
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
  font-weight: 400;
  font-size: 2rem;
  color: #434655;
  padding-left: 20%;
  /* margin-top: 50px; */
}

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

.bold {
  font-weight: 600;
}

@media only screen and (max-width: 768px) {
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
  }
}

.footer {
  /* margin-top: 50px;
  position: fixed;
  bottom: 0;
  margin-bottom: 10px;
  display: flex;
  justify-content: space-around; */
  position: fixed;
	bottom: 45px;
	left: 0;
	right: 0;
	height: 0;
	/* center all inline content */
	text-align: center;
}

.footer a {
  font-size: 1.5em;
  margin: 0 50px;
  /* make the block inline */
	display: inline-block;
	/* reset container's center alignment */
	text-align: left;
}

</style>
<template>
  <div class="root2">
    <div class="container heading">
      <div class="photo">
        <img class="image" src="../assets/about_me_pic.jpg" alt="My Photo">
      </div>
      <div class="intro">
        <div class="intro-heading">Hey<span>,</span> I<span>'</span>m Naveen<span>.</span></div>
        <hr class="material-hr">
        <div class="intro-body pt-3">
          I enjoy turning complex problems into simple, beautiful and intuitive designs. When I'm not coding, building websites, you'll find me designing vector art, making music, editing photos.
        </div>
      </div>
    </div>

    <div class="info">
      <div class="spacer">
        <h1>Hobbies</h1>
        <hr>
        <p>I like to spend my free time by doing things that i love to do. Here are the list of hobbies that i have</p>
      </div>
    </div>

    <div class="hobbies">
      <horizontal-card
        v-for="hobby in hobbies"
        :key="hobby.id"
        :Heading="hobby.title"
        :Body="hobby.body"
        :Picture="hobby.picture"
      >
      </horizontal-card>
    </div>

    <div class="music">
      <p>Who doesn't like music...</p>
      <p>I'm an edm lover and know a little bit of music production</p>
      <p>Check if you and i enjoy the same type</p>
    </div>

    <div class="footer">

      <div class="logo">
        <router-link to="/"><img src="../assets/Logo01.png" alt="Brand-Logo"></router-link>   
      </div>

      <div class="links">
        <a href="mailto:naveenbudhwal@gmail.com">
          <span class="icon">
            <i class="far fa-envelope"></i>
          </span>
        </a>
        <a href="https://www.instagram.com/naveenbudhwal">
          <span class="icon">
            <i class="fab fa-instagram"></i>
          </span>
        </a>
        <a href="https://www.linkedin.com/in/naveenbudhwal">
          <span class="icon">
            <i class="fab fa-linkedin-in"></i>
          </span>
        </a>
        <a href="https://www.github.com/naveenbudhwal">
          <span class="icon">
            <i class="fab fa-github"></i>
          </span>
        </a>
        <a href="https://www.twitter.com/naveenbudhwal">
          <span class="icon">
            <i class="fab fa-twitter"></i>
          </span>
        </a>
      </div>

      <div class="copyright mt-5">
        <p><i class="far fa-copyright"></i> 2019 Naveen Budhwal. All rights reserved</p>
      </div>
    </div>
  </div>
</template>


<script>
import HorizontalCard from '../components/HorizontalCard.vue';

export default {
  name: 'About',
  components: { HorizontalCard },
  data() {
    return {
      hobbies: [
        { id: 1, title: 'Photography', body: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Tempora rem magnam quisquam quasi saepe eligendi numquam maxime pariatur accusamus voluptate.', picture: require('@/assets/photography.png')},
        { id: 2, title: 'Vector Art', body: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Tempora rem magnam quisquam quasi saepe eligendi numquam maxime pariatur accusamus voluptate.', picture: require('@/assets/design.png')},
        { id: 3, title: 'Running', body: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Tempora rem magnam quisquam quasi saepe eligendi numquam maxime pariatur accusamus voluptate.', picture: require('@/assets/running.png')},
        { id: 4, title: 'Gaming', body: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Tempora rem magnam quisquam quasi saepe eligendi numquam maxime pariatur accusamus voluptate.', picture: require('@/assets/gaming.png')}
      ]
    }
  }
}
</script>

<style scoped>

.root2 {
  font-family: "Montserrat", sans-serif;
  line-height: 1.6;
}

.intro {
  margin: 0 10%;
}

.heading {
  display: flex;
  padding: 4% 0;
}

.container {
  font-family: "Montserrat", sans-serif;
  margin-top: 5%;
}

.image {
  width: 270px;
  height: auto;
  -webkit-box-shadow: 0 10px 6px -6px #777;
  -moz-box-shadow: 0 10px 6px -6px #777;
  box-shadow: 0 10px 6px -6px #777;
}

.intro-heading {
  color: #434655;
  font-weight: 500;
  font-size: 2.5em;
}

.intro-body {
  color: #535353;
  font-size: 1.2em;
}

span {
  color: #2b70dc;
}

i {
  color: #2b70dc;
  font-size: 1.5em;
}

.material-hr {
  width: 100px;
  border: 0;
  height: 5px;
  background: #2b70dc;
  border-radius: 7px;
  margin-left: 0;
}

.spacer {
  margin: 0 20%;
}

.info {
  margin: 5% 0;
  padding-top: 5%;
  padding-bottom: 10%; 
  background: #191a1d;
}

hr {
  width: 50%;
  background: rgba(255,255,255,0.1);
  height: 2px;
}

.info h1 {
  color: rgba(255,255,255,0.9);
  text-align: center;
}

.info p {
  text-align: center;
  color: rgba(255,255,255,0.3);
  font-size: 1.3em;
}

.hobbies {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  margin-top: -170px;
  margin-bottom: 5%;
}

.footer {
  /* display: flex; */
  width: 100%;
  margin: 0;
  padding: 2% 15%;
  background: #191a1d;
  color: #fff;
  font-family: "Montserrat", sans-serif;
}

.footer a {
  text-decoration: none;
  /* margin: 0.5em 0; */
}

.footer .links a i:hover {
  color: #2b70dc;
  background: #fff;
}

.footer .links {
  display: flex;
  justify-content: space-around;
  margin: 0 100px;
}

.links a i {
  padding: 10px;
  border: 2px solid rgba(255,255,255,0.3);
  border-radius: 100%;
  font-size: 22px;
  width: 48px;
  height: 48px;
  color: rgba(255,255,255,1);
  transition: all 0.2s ease-in-out;
  display: flex;
  justify-content: center;
  align-items: center;
}

.logo {
  /* flex: 1;
  margin: auto; */
  width: fit-content;
  margin: 0 auto;
  padding: 10px 0;
}

.logo img {
  width: 200px;
  height: auto;
}

.copyright {
  text-align: center;
  color: #434655;
}

.copyright p i {
  color: #434655;
  font-size: 18px;
}

::-moz-selection { /* Code for Firefox */
  color: #000;
  background: rgba(0,0,0,0.3);
}

::selection {
  color: #000;
  background: rgba(0,0,0,0.3);
}

@media only screen and (max-width: 768px) {
  .container {
    flex-direction: column;
  }
  .image {
    margin-bottom: 8%;
  }
  .photo, .intro {
    margin: 0 auto;
  }
  .intro-heading {
    text-align: center;
    margin-bottom: 20px;
  }
  .intro-body {
    text-align: center;
    padding: 0 20px;
    margin-bottom: 50px;
  }
  .info {
    padding-top: 50px;
    padding-bottom: 150px;
  }
  .hobbies {
    margin-top: -130px;
  }
  hr {
    text-align: center;
  }
  .material-hr {
    margin: auto;
  }
}

@media only screen and (max-width: 576px) {
  .footer .links a {
    margin: 0 7px;
  } 
}

@media only screen and (max-width: 1200px) {
  .hobbies {
    margin-top: -120px;
  }
}

</style>
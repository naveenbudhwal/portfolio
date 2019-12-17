<template>
  <div class="root">
    <div class="header">
      <div class="heading">Skills</div>
      <!-- <hr /> -->
    </div>
    <div class="container page">
      <card  
      v-for="skill in skills"
      :key="skill.id"
      :Heading="skill.title"
      :skillBody="skill.body"
      :Picture="skill.picture"
      ></card>
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
import Card from "../components/Card.vue";

export default {
  name: "Skills",
  components: { Card },
  data() {
    return {
      skills: [
      { id: 1, title: 'WEB DEVELOPMENT', body: ["Vue JS", "Node JS", "MongoDB", "Express JS"], picture: require('@/assets/web_dev.png')},
      { id: 2, title: 'DESIGNING', body: ["Abobe Illustrator", "Adobe Photoshop", "Adobe Premiere Pro", "Adobe Lightroom"], picture: require('@/assets/design.png')},
      { id: 3, title: 'MUSIC PRODUCTION', body: ["FL Studio"], picture: require('@/assets/music_prod.png')},
      {id: 4, title: 'PROGRAMMING', body: ['C / C++', 'Python'], picture: require('@/assets/programming.png')}
    ]
    };
  }
};
</script>

<style scoped>

.container {
  display: flex;  
}

.header {
  background: rgba(0,123,255,.5);
  margin-top: -140px;
}

.heading {
  font-family: "Montserrat", sans-serif;
  font-size: 3em;
  font-weight: 600;
  color: #F6F8FF;
  /* margin-left: 20%; */
  text-align: center;
  padding-top: 10%;
  padding-bottom: 6rem;
}

/* hr {
  width: 60%;
  background: #000;
} */

.container, .page {
  margin-top: -70px;
}

i {
  color: #2b70dc;
}

.social-media-bar {
  position: relative;
  height: 50px;
  margin-top: 30px;
  margin-bottom: 10px;
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

@media only screen and (max-width: 1200px) {
  .container {
    flex-direction: column;
    align-items: center;
  }
  .header {
    margin-top: -250px;
  }
  .heading {
    padding-top: 30%;
  }
}

@media only screen and (max-width: 576px) {
  .header {
    margin-top: -300px
  }
  .heading {
    padding-top: 70%;
  }
}

@media only screen and (max-width: 768px) {
  .social-media-bar a {
    margin: 0 10px;
  }
  .social-media-bar {
    margin-bottom: 20px;
  }
}

</style>
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
  font-weight: 700;
  color: #fff;
  margin-left: 20%;
  padding-top: 12%;
  padding-bottom: 5rem;
}

/* hr {
  width: 60%;
  background: #000;
} */

.container, .page {
  margin-top: -70px;
}

@media only screen and (max-width: 768px) {
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

</style>
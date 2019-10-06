<template>
  <div class="root">
    <div class="header">
      <div class="heading">Skills</div>
      <hr />
    </div>
    <div class="container page">
      <skill-card  
      v-for="skill in skills"
      :key="skill.id"
      :skillHeading="skill.title"
      :skillBody="skill.body"
      :skillPicture="skill.picture"
      ></skill-card>
    </div>
  </div>
  
</template>

<script>
import SkillCard from "../components/SkillCard.vue";

export default {
  name: "Skills",
  components: { SkillCard },
  data() {
    return {
      skills: [
      { id: 1, title: 'Web Development', body: ["VueJS", "NodeJS", "MongoDB", "ExpressJS"], picture: require('@/assets/web_dev.png')},
      { id: 2, title: 'Designing', body: ["Abobe Illustrator", "Adobe Photoshop", "Adobe Premiere Pro", "Adobe Lightroom"], picture: require('@/assets/design.png')},
      { id: 3, title: 'Music Production', body: ["FL Studio"], picture: require('@/assets/music_prod.png')},
      {id: 4, title: 'Programming', body: ['C / C++', 'Python'], picture: require('@/assets/programming.png')}
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
  font-weight: 500;
  color: #fff;
  margin-left: 20%;
  padding-top: 12%;
  padding-bottom: 50px;
}

hr {
  width: 80%;
}

.container, .page {
  margin-top: -70px;
}

@media only screen and (max-width: 768px) {
  .container {
    flex-direction: column;
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
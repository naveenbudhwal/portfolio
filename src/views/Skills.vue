<template>
  <div class="skills-page">
    <div class="heading">Skills</div>
    <div class="container">
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
        {
          id: 1,
          title: "WEB DEVELOPMENT",
          body: ["Vue JS", "Node JS", "MongoDB", "Express JS"],
          picture: require("@/assets/web_dev.png")
        },
        {
          id: 2,
          title: "DESIGNING",
          body: [
            "Abobe Illustrator",
            "Adobe Photoshop",
            "Adobe Premiere Pro",
            "Adobe Lightroom"
          ],
          picture: require("@/assets/design.png")
        },
        {
          id: 3,
          title: "MUSIC PRODUCTION",
          body: ["FL Studio"],
          picture: require("@/assets/music_prod.png")
        },
        {
          id: 4,
          title: "PROGRAMMING",
          body: ["C / C++", "Python"],
          picture: require("@/assets/programming.png")
        }
      ]
    };
  }
};
</script>

<style scoped>

.skills-page {
  height: 85vh;
  display: flex;
  flex-direction: column;
  align-items: center;
}

.container {
  display: flex;
  width: 80%;
}

.heading {
  font-size: 3em;
  font-weight: 600;
  color: #333;
  text-align: center;
  margin: 1em 0;
}

i {
  color: #2b70dc;
}

@media only screen and (max-width: 1200px) {
  .skills-page {
    height: 100%;
  }
  .container {
    flex-direction: column;
    align-items: center;
    width: 60%;
  }
}

@media only screen and (max-width: 768px) {
  .container {
    width: 80%;
  }
}
</style>
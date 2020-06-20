<template>
  <div class="root2">
    <div class="heading">
      <div class="photo">
        <img class="image" src="../assets/about_me_pic.jpg" alt="My Photo" />
      </div>
      <div class="intro">
        <div class="intro-heading">
          Hey<span class="color">,</span> I<span class="color">'</span>m Naveen<span class="color">.</span>
        </div>
        <hr class="material-hr" />
        <div class="intro-body pt-3">
          <p>I enjoy making simple, beautiful designs for complex problems.</p>
          <p>Tech Enthusiast.</p>
          <p>EDM Lover.</p>
          <p>Console Gamer.</p>
        </div>
      </div>
    </div>

    <div class="info">
      <div class="spacer">
        <h1>Hobbies</h1>
        <hr />
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
      ></horizontal-card>
    </div>

    <div class="music">
      <p>Who doesn't like music...</p>
      <p>
        I'm an
        <span class="standout">EDM</span> lover and know a little bit of music production
      </p>
      <p>Check if you and i enjoy the same type</p>
      <a href="https://open.spotify.com/user/naveenbudhwal?si=MI1L3rhZQ4iK6qMCCeWScw">
        <span>Spotify</span>
      </a>
    </div>

    <div class="footer">
      <div class="logo1">
        <router-link to="/">
          <img src="../assets/Logo01.png" alt="Brand-Logo" />
        </router-link>
      </div>

      <div class="qoute">
        <p>Do what you love</p>
        <p>& Love what you do</p>
      </div>

      <div class="links">
        <a href="mailto:naveenbudhwal@gmail.com" target="_blank" rel="noopener">
          <span class="icon">
            <i class="far fa-envelope"></i>
          </span>
        </a>
        <a href="https://www.instagram.com/naveenbudhwal" target="_blank" rel="noopener">
          <span class="icon">
            <i class="fab fa-instagram"></i>
          </span>
        </a>
        <a href="https://www.linkedin.com/in/naveenbudhwal" target="_blank" rel="noopener">
          <span class="icon">
            <i class="fab fa-linkedin-in"></i>
          </span>
        </a>
        <a href="https://www.github.com/naveenbudhwal" target="_blank" rel="noopener">
          <span class="icon">
            <i class="fab fa-github"></i>
          </span>
        </a>
        <a href="https://www.twitter.com/naveenbudhwal" target="_blank" rel="noopener">
          <span class="icon">
            <i class="fab fa-twitter"></i>
          </span>
        </a>
      </div>
      <div class="credits">
        <div class="icon-credits">
          Icons from
          <a
            href="https://www.fontawesome.com"
            class="color"
            target="_blank"
            rel="noopener"
          >
            Font Awesome
            <i class="fab fa-font-awesome-flag"></i>
          </a>
        </div>
      </div>
      <div class="copyright">
        <p>
          <i class="far fa-copyright"></i>
          {{year}} Naveen Budhwal. All rights reserved
        </p>
      </div>
    </div>
  </div>
</template>


<script>
import HorizontalCard from "../components/HorizontalCard.vue";

const vectorArt =
  "Recently I discovered my love for Adobe Illustrator. It is really fun to create and play with vector objects.";

const running =
  "When I'm not on my computer, I go for solid run on the field. It clears up your mind and good for your health.";

const gaming =
  "I have been playing console games since my childhood. Big fan of the GTA series and Call of Duty lineup. Waiting for the release of the next playstation.";

let d = new Date();
let y = d.getFullYear();

export default {
  name: "About",
  components: { HorizontalCard },
  data() {
    return {
      year: y,
      hobbies: [
        {
          id: 1,
          title: "Vector Art",
          body: vectorArt,
          picture: require("@/assets/design.png")
        },
        {
          id: 2,
          title: "Running",
          body: running,
          picture: require("@/assets/running.png")
        },
        {
          id: 3,
          title: "Gaming",
          body: gaming,
          picture: require("@/assets/gaming.png")
        }
      ]
    };
  }
};
</script>

<style scoped>
.root2 {
  line-height: 1.6;
}

.intro {
  margin: 0 10%;
}

.heading {
  display: flex;
  padding: 4% 0;
  justify-content: center;
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
  font-weight: 500;
  font-size: 1.2em;
}

.color {
  color: #2b70dc;
}

.standout {
  color: #2a6461;
  font-weight: 600;
  font-size: 1.2em;
}

i {
  color: #2b70dc;
  font-size: 1.5em;
}

.material-hr {
  width: 100px;
  border: 0;
  height: 7px;
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
  background: rgba(255, 255, 255, 0.1);
  height: 3px;
  border: none;
}

.info h1 {
  color: rgba(255, 255, 255, 0.9);
  text-align: center;
  font-weight: 500;
  font-size: 2em;
}

.info p {
  text-align: center;
  color: rgba(255, 255, 255, 0.5);
  font-size: 1.2em;
  padding: 0 40px;
}

.hobbies {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  margin-top: -170px;
  margin-bottom: 5%;
}

.music {
  background: #e6f4f1;
  margin: 10% 10%;
  padding: 5% 10%;
  color: #389b97;
  font-weight: 500;
  font-size: 1.1em;
  text-align: center;
  border-radius: 20px;
}

.music a {
  text-decoration: none;
  background: #1db954;
  color: #fff;
  display: flex;
  width: 200px;
  margin: 0 auto;
  margin-top: 40px;
  box-shadow: 0 3px 5px -1px rgba(0, 0, 0, 0.2),
    0 6px 10px 0 rgba(0, 0, 0, 0.14), 0 1px 18px 0 rgba(0, 0, 0, 0.12);
  padding: 10px 20px;
  border-radius: 24px;
  transition: all 0.2s ease-in-out;
}

.music a span {
  color: #fff;
  font-size: 0.9em;
  flex: 1;
  text-align: center;
  text-transform: uppercase;
  letter-spacing: 2px;
}

.music a:hover {
  background: #248c88;
}

.footer {
  width: 100%;
  margin: 0;
  background: #191a1d;
  color: #fff;
}

.qoute {
  text-align: center;
  color: rgba(255, 255, 255, 0.6);
  font-size: 1.3em;
  font-weight: 400;
  margin-bottom: 40px;
  margin-top: -20px;
}

.footer a {
  text-decoration: none;
}

.footer .links a i:hover {
  color: #2b70dc;
  background: #fff;
}

.footer .links {
  display: flex;
  width: 60%;
  justify-content: space-around;
  margin: 0 auto;
}

.links a i {
  padding: 10px;
  border: 2px solid rgba(255, 255, 255, 0.3);
  border-radius: 100%;
  font-size: 22px;
  width: 34px;
  height: 34px;
  color: rgba(255, 255, 255, 1);
  transition: all 0.2s ease-in-out;
  display: flex;
  justify-content: center;
  align-items: center;
}

.logo1 {
  width: fit-content;
  margin: 0 auto;
  padding: 10px 0;
}

.logo1 img {
  width: 200px;
  height: auto;
}

.icon-credits {
  text-align: center;
  padding: 40px 0 10px 0;
  color: #434655;
}

.icon-credits i {
  padding: 0 5px;
  cursor: pointer;
}

.copyright {
  text-align: center;
  color: #434655;
  padding-bottom: 10px;
}

.copyright p i {
  color: #434655;
  font-size: 18px;
}

.color {
  color: #2b70dc;
}

@media only screen and (max-width: 768px) {
  .heading {
    flex-direction: column;
  }
  .image {
    width: 250px;
    height: auto;
    margin-bottom: 8%;
  }
  .photo,
  .intro {
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
  .info p {
    padding: 0;
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
  .intro {
    padding: 0 10px;
  }
  .intro-heading {
    font-size: 2.2em;
  }
  .intro-body {
    font-size: 1.17em;
  }
  .image {
    width: 200px;
    height: auto;
  }
  .footer .links a {
    margin: 0 7px;
  }
  .links a i {
    width: 30px;
    height: 30px;
  }
}

@media only screen and (max-width: 370px) {
  .footer .links a {
    margin: 0 3px;
  }
  .links a i {
    width: 25px;
    height: 25px;
  }
  .music a {
    width: 150px;
  }
}

@media only screen and (max-width: 1200px) {
  .hobbies {
    margin-top: -150px;
  }
  .heading {
    justify-content: center;
  }
  .heading .intro {
    margin: 0 3%;
  }
}
</style>
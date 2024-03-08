<template>
  <v-app>
    <div class="mall">
      <div>
        <FreeYoutubeVideos />
      </div>

      <div>
        <About />
      </div>

      <Premium />

      <div class="block outlined">
        <Testinomials />
      </div>
      <Disclaimer />
      <!-- <h3>Blogs</h3> -->

      <Foot />
    </div>
  </v-app>
</template>

<script>
import FreeYoutubeVideos from "../components/Free-Youtube-Videos";
import Foot from "../components/Footer";

import Testinomials from "@/components/Testinomials.vue";
import Premium from "@/components/Premium.vue";
import Disclaimer from "@/components/Disclaimer.vue";
import About from "../components/About.vue";
export default {
  name: "Home-page",

  components: {
    FreeYoutubeVideos,
    Foot,
    Testinomials,
    Premium,
    About,
    Disclaimer,
  },
  methods: {
    scrollItem(ref) {
      const el = document.getElementById(ref);
      el.scrollIntoView({ behavior: "smooth" });
    },
  },
};
</script>



<style>
.blogs {
  margin-top: 20px;
  flex-grow: 1;
  background-color: rgba(255, 255, 255, 0.5);
  border-radius: 30%;
}
.foot {
  background-color: black;
  background-size: cover;
}

.mtop {
  margin-top: 100px;
}

.mbottom {
  margin-bottom: 100px;
}

.theme--light.v-sheet--outlined.mobile {
  border: 2px solid black !important;
}

#app {
  font-family: Arial, Helvetica, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #42b983;
  display: flex;
  flex-direction: column;
  /* z-index:100; */
  /* position:relative; */
  /* fallback for old browsers */
}
</style>
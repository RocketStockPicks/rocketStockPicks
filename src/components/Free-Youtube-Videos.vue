<template>
  <div>
    <v-card class="learn-videos-title mt-10">
      <h1
        style="
          color: rgb(70, 0, 7);
          margin-top: 1%;
          margin-bottom: 3%;
          letter-spacing: 2px;
        "
      >
        LEARN MORE FROM VIDEOS
      </h1>
      <v-expansion-panels
        mandatory
        style="margin-top: 3%; margin-bottom: 3%"
        v-model="panel"
      >
        <v-overlay activator="parent"
          v-model="overlay"
          class="align-center justify-center"
          location-strategy="connected"
          scroll-strategy="block" opacity="0.6" 
          
        >
          <v-progress-circular color="primary" size="50" width="4" >please wait...</v-progress-circular>
        </v-overlay>
        <v-expansion-panel
          v-for="(detail, index) in map"
          :key="index"
          :value="detail.id"
          @click="readAuthors(detail.id)"
        >
          <v-expansion-panel-header>
            <h2 style="text-align: left; color: Brown">
              <v-icon color="green"> fa-arrow-down</v-icon> {{ detail.title }}
            </h2>
          </v-expansion-panel-header>
          <v-expansion-panel-content>
            <div
              class="m-5"
              style="margin-bottom: 2%; margin-top: 2%; text-align: center"
            ></div>
            <v-row no-gutters>
              <v-col
                cols="12"
                sm="6"
                xs="6"
                v-for="(item, index) in expandable.items"
                :key="index"
              >
                <iframe
                  width="95%"
                  height="315"
                  :src="
                    'https://youtube.com/embed/' + item.contentDetails.videoId
                  "
                  title="YouTube video player"
                  frameborder="0"
                  allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share"
                  allowfullscreen
                ></iframe>
              </v-col>
            </v-row>

            <v-row justify="center" style="margin-bottom: 3%; margin-top: 3%"
              ><v-btn
                :href="
                  'https://youtube.com/playlist?list=' +
                  detail.id +
                  '&feature=shared'
                "
                class="deep-purple accent-4 dark text-white"
                target="_blank"
                ><span style="color: white"> VIEW ALL</span>
              </v-btn></v-row
            >
            <!-- </v-tab-item> -->
            <!-- <v-tab-item>
        <div
          class="m-5"
          style="margin-bottom: 2%; margin-top: 2%; text-align: center"
        >
          <h3>
            &nbsp;
            <span style="color: green" class="dark">Positional Trading </span>
            is a trading strategy in which traders hold their positions for an
            extended period, typically from several weeks to months or even
            years.
          </h3>
        </div>
        <v-row no-gutters style="height: 450px">
          <v-col cols="12" sm="6" xs="6">
            <iframe
              height="95%"
              width="80%"
              src="https://www.youtube.com/embed/AvUYV-klssw?si=13vziJ7mrs8yZgh1"
              title="YouTube video player"
              frameborder=""
              allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share"
              allowfullscreen
            ></iframe>
          </v-col>

          <v-col cols="12" sm="6" xs="6">
            <iframe
              height="95%"
              width="80%"
              src="https://www.youtube.com/embed/2LlKm5ldIr8?si=k_6_lbUa81X-jg9v"
              title="YouTube video player"
              frameborder="0"
              allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share"
              allowfullscreen
            ></iframe>
          </v-col>
        </v-row>

        <v-row justify="center" style="margin-bottom: 3%; margin-top: 3%"
          ><v-btn class="deep-purple accent-4 dark text-white"
            ><span style="color: white"> VIEW ALL</span>
          </v-btn></v-row
        >
      </v-tab-item>
      <v-tab-item>
        <div
          class="m-5"
          style="margin-bottom: 2%; margin-top: 2%; text-align: center"
        >
          <h3>
            &nbsp;
            <span style="color: green" class="dark">Positional Trading </span>
            is a trading strategy in which traders hold their positions for an
            extended period, typically from several weeks to months or even
            years.
          </h3>
        </div>
        <v-row no-gutters style="height: 450px">
          <v-col cols="12" sm="6" xs="6">
            <iframe
              height="95%"
              width="80%"
              src="https://www.youtube.com/embed/AvUYV-klssw?si=13vziJ7mrs8yZgh1"
              title="YouTube video player"
              frameborder=""
              allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share"
              allowfullscreen
            ></iframe>
          </v-col>

          <v-col cols="12" sm="6" xs="6">
            <iframe
              height="95%"
              width="80%"
              src="https://www.youtube.com/embed/2LlKm5ldIr8?si=k_6_lbUa81X-jg9v"
              title="YouTube video player"
              frameborder="0"
              allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share"
              allowfullscreen
            ></iframe>
          </v-col>
        </v-row>

        <v-row justify="center" style="margin-bottom: 3%; margin-top: 3%"
          ><v-btn class="deep-purple accent-4 dark text-white"
            ><span style="color: white"> VIEW ALL</span>
          </v-btn></v-row
        >
      </v-tab-item>
      <v-tab-item>
        <div
          class="m-5"
          style="margin-bottom: 2%; margin-top: 2%; text-align: center"
        >
          <h3>
            &nbsp;
            <span style="color: green" class="dark">Positional Trading </span>
            is a trading strategy in which traders hold their positions for an
            extended period, typically from several weeks to months or even
            years.
          </h3>
        </div>
        <v-row no-gutters style="height: 450px">
          <v-col cols="12" sm="6" xs="6">
            <iframe
              height="95%"
              width="80%"
              src="https://www.youtube.com/embed/AvUYV-klssw?si=13vziJ7mrs8yZgh1"
              title="YouTube video player"
              frameborder=""
              allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share"
              allowfullscreen
            ></iframe>
          </v-col>

          <v-col cols="12" sm="6" xs="6">
            <iframe
              height="95%"
              width="80%"
              src="https://www.youtube.com/embed/2LlKm5ldIr8?si=k_6_lbUa81X-jg9v"
              title="YouTube video player"
              frameborder="0"
              allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share"
              allowfullscreen
            ></iframe>
          </v-col>
        </v-row>

        <v-row justify="center" style="margin-bottom: 3%; margin-top: 3%"
          ><v-btn class="deep-purple accent-4 dark text-white"
            ><span style="color: white"> VIEW ALL</span>
          </v-btn></v-row
        >
      </v-tab-item>
      <v-tab-item>
        <div
          class="m-5"
          style="margin-bottom: 2%; margin-top: 2%; text-align: center"
        >
          <h3>
            &nbsp;
            <span style="color: green" class="dark">Positional Trading </span>
            is a trading strategy in which traders hold their positions for an
            extended period, typically from several weeks to months or even
            years.
          </h3>
        </div>
        <v-row no-gutters style="height: 450px">
          <v-col cols="12" sm="6" xs="6">
            <iframe
              height="95%"
              width="80%"
              src="https://www.youtube.com/embed/AvUYV-klssw?si=13vziJ7mrs8yZgh1"
              title="YouTube video player"
              frameborder=""
              allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share"
              allowfullscreen
            ></iframe>
          </v-col>

          <v-col cols="12" sm="6" xs="6">
            <iframe
              height="95%"
              width="80%"
              src="https://www.youtube.com/embed/2LlKm5ldIr8?si=k_6_lbUa81X-jg9v"
              title="YouTube video player"
              frameborder="0"
              allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share"
              allowfullscreen
            ></iframe>
          </v-col>
        </v-row>

        <v-row justify="center" style="margin-bottom: 3%; margin-top: 3%"
          ><v-btn class="deep-purple accent-4 dark text-white"
            ><span style="color: white"> VIEW ALL</span>
          </v-btn></v-row
        >
      </v-tab-item>
    </v-tabs> -->
          </v-expansion-panel-content>
        </v-expansion-panel>
      </v-expansion-panels>
    </v-card>
  </div>
</template>
  
<script>
import axios from "axios";

export default {
  data() {
    return {
      expandable: {},
      map: [
        {
          title: "TRADING CONCEPTS",
          id: "PLsHNXHp8BW0B4Ds23U0s55C_RCV1GLYKS",
        },
        {
          title: "SIMPLE TRADING STRATEGIES",
          id: "PLsHNXHp8BW0DMVEJdD1yYZCSCPhsHJoR2",
        },
        {
          title: "OPTIONS TRADING",
          id: "PLsHNXHp8BW0CXVaBcuA0pbWdRkVRYUROC",
        },
        {
          title: "OVERALL MARKET UPDATE",
          id: "PLsHNXHp8BW0CfUo5M5P6LTdZMZKOJD39l",
        },
        {
          title: "ROCKET SUCCESS STORIES",
          id: "PLsHNXHp8BW0DFnPJeIA9rprCj4f-7X70o",
        },
      ],
      overlay: false,
    };
  },
  methods: {
    readAuthors: async function (id) {
      this.overlay = true;
      axios
        .get(
          "https://youtube.googleapis.com/youtube/v3/playlistItems?playlistId=" +
            id +
            "&key=AIzaSyDL-9ERf_tB09pDtdv-De2Cfyv7BIlA8UQ&part=contentDetails&maxResults=2"
        )
        .then((response) => {
          console.log(response.data);
          this.expandable = response.data;
          this.overlay=false;
         
        })
        .catch((error) => {
          console.log(error);
          this.overlay = false;
        });
    },
  },
  mounted() {
    axios
      .get(
        "https://youtube.googleapis.com/youtube/v3/playlistItems?playlistId=PLsHNXHp8BW0AHPtb2K1npfOhmipCUOSRt&key=AIzaSyDL-9ERf_tB09pDtdv-De2Cfyv7BIlA8UQ&part=contentDetails&maxResults=2"
      )
      .then((response) => {
        this.expandable = response.data;
        console.log(this.expandable);
      })
      .catch((error) => {
        console.log(error);
      });
  },
};
</script>

<style scoped>
.card {
  min-width: 90%;
}

.main-row {
  height: 100%;
  justify-content: space-evenly;
}
.container {
  height: 100%;
}
.learn-videos-title {
  font-family: Cambria, Cochin, Georgia, Times, "Times New Roman", serif;
  font-size: 20 px;
}
</style>
<template>
  <div class="foot-r">
    <v-row  class="foot-row d-flex">
      <v-col class="col-xs-12" lg="4" sm="12" md="12" >
        <v-icon s="white" class="mx-4 white--text">mdi-copyright </v-icon>
       <span style="color:white;"> All Right Reserved - RocketStockPicks</span>
      </v-col>

      <v-col class="col-xs-12 d-flex" lg="4" sm="12" md="12" >
        <v-btn
          :href="icon.url"
          target="_blank"
          v-for="icon in icons"
          :key="icon.id"
          class="mx-4 white--text"
          icon
        >
          <v-icon size="20px">
            {{ icon.id }}
          </v-icon>
        </v-btn>
      </v-col>
      

      <v-col class="col-xs-12" lg="4" sm="12" md="12">
        <strong> info@rocketstockpicks.co.in </strong>
      </v-col>
    </v-row>
 <v-row  class="foot-row d-flex" justify="center">
    <img
      src="https://hitwebcounter.com/counter/counter.php?page=11793020&style=0023&nbdigits=8&type=page&initCount=0"
      title="Counter Widget"
      Alt="Visit counter For Websites"
      border="2"
    />
 </v-row>
  </div>
</template>
  
<script>
export default {
  data: () => ({
    icons: [
      {
        id: "fab fa-facebook",
        url: "https://www.facebook.com/RocketStockPicks",
      },
      {
        id: "fab fa-twitter",
        url: "https://twitter.com/bittu_grd",
      },

      {
        id: "fab fa-youtube",
        url: "https://youtube.com/@RocketStockPicks",
      },

      {
        id: "mdi-instagram",
        url: "https://www.instagram.com/rocketstockpicks/",
      },
    ],
  }),
};
</script>

<style scoped>
.foot-r {
  background-size: fill;
  background-color: #1da1f2;
  width: 100%;
}
.col {
  flex-wrap: nowrap;
  justify-content: center;
}
strong {
  color: white;
}
.col{
  flex-basis: auto;
}
</style>
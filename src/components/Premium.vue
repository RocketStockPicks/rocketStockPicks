<template>

  <v-container  class="lighten-5" >
    <div class="content" >
    <h2 class="lighten-5" style="color:black;margin-bottom:2%;margin-top:2%">SET YOUR EXPECTATIONS RIGHT</h2>
    <v-divider></v-divider>
    <v-row max-width="100%" >
      <v-col cols="12" sm="6">
        <v-card class=" mx-auto" max-width="100%" tile>
          <v-list lines="two">
            <h3 style="color:green;"> WHAT TO EXPECT</h3>
            <v-list-item
              class="text-black"
              v-for="item in items"
              :key="item.expected"
             :v-if="item.expected != null"
            >
              <v-list-item-icon  v-if="item.expected != null" style="margin-left:0%">
               <i class="fa-solid fa-check"></i>
              </v-list-item-icon>
              <v-list-item-content style="margin-left:0%">
                <v-list-item-title class="text-wrap text-left">{{ item.expected }}</v-list-item-title>
              </v-list-item-content>
            </v-list-item>
          </v-list>
        </v-card>
      </v-col>
      <v-col cols="12" sm="6" >
        <v-card class="mx-auto" max-width="100%" min-height="100%" tile>
          <v-list lines="two">
            <h3 class="align-left" style="color:orange;"> WHAT NOT TO EXPECT</h3>
            <v-list-item
              class="text-black"
              v-for="item in items"
              :key="item.unexpected"
            >
              <v-list-item-icon style="margin-left:0%"> 
               <i class="fa-solid fa-xmark"></i>
              </v-list-item-icon>
              <v-list-item-content style="margin-left:0%">
                <v-list-item-title class="text-left text-wrap"> {{ item.unexpected }}</v-list-item-title>
              </v-list-item-content>
            </v-list-item>
          </v-list>
        </v-card>
      </v-col>
    </v-row>

    <v-row class="join-button" max-width="100%" height="40px"  align="center" justify="space-around" >
      <v-btn href="https://t.me/RocketStockPicks" large class="blue" min-height="100%" style="color: white; align : centre" >
        <b>JOIN OUR TELGRAM GROUP</b> <v-icon>fab fa-telegram </v-icon></v-btn
      >
    </v-row>
    </div>
  </v-container>
</template>
<script>
export default {
  data() {
    return {
      items: [
        {
          expected:
            "Focus on learning price-action and simple trading strategies",
          unexpected: "No Portfolio Management at any stage ",
        },
        {
          expected:
            "Our views on selected Stocks and Indices, with emphasis on Technical Analysis",
          unexpected: "No promises on making money",
        },
        {
          expected:
            "Occassional audio/video updates on our Telegram or Youtube channel",
          unexpected: "No obligation on number of learning posts",
        },
        {
          expected:
            "Subscription renewal in 30 days",
          unexpected: "Spoon feeding, learn basic before you join",
        },
        {
          
          unexpected: "Refund of monthly training fee",
        },
      ],
    };
  },
};
</script>
<style scoped>
.join-button{
    margin-top: 30px;

}
.align-left{
    -ms-text-align-last: left;
  
}
</style>
<template>
  <div
    ref="about-us"
    id="about-us"
    class="about-us"
    style="color: white; background-color: rgb(10, 10, 39)">
    <h1 style="padding-top:2%;margin-bottom:2%; letter-spacing: 1px">RAMBAAN STRATEGY</h1>
    <hr />
    <v-row class="navy">
      <v-col cols="12" sm="6" style="height: 60vh">
        <img class="about-image" src="../assets/about-us-2.jpeg" />
      </v-col>
      <v-col cols="12" sm="6" class="about-class">
        <div class="about-content">
          <p>
            We have been following the financial markets and geopolitics for
            combined <b style="font-size: 25px">15+ </b> years now and have a
            solid understanding of technical analysis using candlestick chart
            pattern and Python/Pinescript programming languages.
          </p>

          <p>
            Our <b style="font-size: 25px">'RamBaan Strategy'</b> coded on
            TradingView is a one stop shop for identifying the best entry,
            re-entry and exit for trading and investing positions.*
          </p>

          <div class="copy-right d-flex text-wrap">
            <i class="fa fa-copyright fa-2x"></i>
            <div style="min-height: 30px" class="text-wrap">
              Application number to copyright RamBaan Strategy:202231038788
            
            </div>
          </div>

          <!-- <div class="social-media-icons d-flex">
            <p>
              <a href="https://twitter.com/bittu_grd" target="_blank"
                ><i class="fab fa-twitter fa-2x" style="color: #1da1f2"></i
              ></a>
            </p>
            <p>
              <a
                href="https://www.youtube.com/@RocketStockPicks"
                target="_blank"
                ><i class="fab fa-youtube fa-2x" style="color: red"></i
              ></a>
            </p>
          </div> -->
        </div>
      </v-col>
    </v-row>
  </div>
</template>
<style scoped>
.row {
  align-items: center;
}

p.small {
  line-height: 0.8;
}

p.big {
  line-height: 1.8;
}
h2 {
  margin-bottom: 2%;
}

a:link {
  text-decoration: none;
}

a:visited {
  text-decoration: none;
}
a:hover {
  text-decoration: underline;
}

a:active {
  text-decoration: underline;
}

.fa-twitter:hover {
  transform: scale(1.2);
}

.fa-youtube:hover {
  transform: scale(1.2);
}
.about-content {
  align-content: center;
  font-family: Cambria, Cochin, Georgia, Times, "Times New Roman", serif;
  font-size: 20px;
}
.social-media-icons {
  margin-top: 4%;
  justify-content: space-evenly;
  margin-bottom: -10px;
}

.copy-right {
 
  align-items: center;
  justify-content: space-evenly;
}
.about-image {
  object-fit: contain;
  min-width: 100%;
  min-height: 100%;
  max-height: 100%;
  contain: size;
}

.about-class {
  margin-top: 1%;
  margin-bottom: 3%;
 
}
.about-us{
  font-family: Cambria, Cochin, Georgia, Times, "Times New Roman", serif;
  font-size: 20px;
}
</style>
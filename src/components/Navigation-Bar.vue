<template>
  <div class="containers">
    <div >
    <v-btn class="mx-2" large style="color: white" text> <h3>Home</h3> </v-btn>
    <v-btn @click="scrollItem('about-us')" class="nav-btn"  style="color: white" text> <h3>About</h3> </v-btn>
    </div>
    <div class="nav-bar">
      <img class="rocket-image" src="../assets/up.gif" />
    </div>
  </div>
</template>

<script>
export default{
   methods:{
    scrollItem(ref){
const el = document.getElementById(ref);
      el.scrollIntoView({behavior: "smooth"});
      
    }
  }
}

</script>

<style>
.round {
  border-radius: 100%;
  /* margin-left:20% ; */
}
.containers {
  background-color: black;
  background-size: cover;
  justify-content: center;
  
  
}

.main-contents {
  background-color: rgb(46, 45, 45);
}
.rocket-image {
  height: 100%;
  width: 100%;
  max-height: 600px;
  object-fit: fill;
}
.nav-bar {
  object-fit: fill;
}
.nav-btn{
transform-style: flat;
}


</style> 
<template>
  <div>
    <div class="landing-collage">
      <img @click="navigateTo('planet')" class="landing-img moon" src="../../../images/moon.png" alt="">
      <!-- <img @click="navigateTo('planet')" class="landing-img dagobah" src="../../../images/planet-dagobah.png" alt=""> -->
      <!-- <img @click="navigateTo('starships')" class="landing-img tie-bomber" src="../../../images/tie-bomber.png" alt=""> -->
      <img @click="navigateTo('character')" class="landing-img darth" src="../../../images/darth-vader.png" alt="">
      <!-- <img @click="navigateTo('character')" class="landing-img leia" src="../../../images/leia.png" alt=""> -->
      <img @click="navigateTo('character')" class="landing-img luke" src="../../../images/luke.png" alt="">
      <!-- <img @click="navigateTo('starships')" class="landing-img r2-d2" src="../../../images/R2-D2.png" alt=""> -->
      <!-- <img @click="navigateTo('character')" class="landing-img c-3po" src="../../../images/C-3PO.png" alt=""> -->
      <!-- <img @click="navigateTo('starships')" class="landing-img y-wing" src="../../../images/y-wing.png" alt=""> -->
      <!-- <img @click="navigateTo('starships')" class="landing-img x-wing" src="../../../images/x-wing.png" alt=""> -->
    </div>
  </div>
</template>

<script>
export default {
  name: "Home",
  data: function() {
    return {
   
    };
  },
  methods: {
    navigateTo: function(type) {
      this.$router.push({ name: "detail", params: { type: type } });
    }
  },
  created: function() {
   
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.landing-img{
  /* max-width: 400px; */
  position: absolute;
}

.moon{
  z-index: 1;
  max-width: 400px;
  left: calc(50vw - 100px);
}

.dagobah{
  z-index: 2;
  max-width: 200px;
  right: calc(50vw - 10px);
}

.tie-bomber{
  z-index: 3;
}

.darth{
  z-index: 4;
  max-width: 900px;
  right: calc(50vw - 550px);
}

.leia{
  z-index: 5;
}

.luke{
  z-index: 6;
  max-width: 400px;
  left: (50vw - 200px);
  right: (50vw - 200px)
}

.r2-d2{
  z-index: 7;
}

.c-3po{
  z-index: 8;
}

.y-wing{
  z-index: 9;
}

.x-wing{
  z-index: 10;
}



</style>
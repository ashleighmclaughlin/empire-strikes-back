<template>
<<<<<<< HEAD
=======

>>>>>>> e813f579c42e6e61e0147a6bbeeeb735a3d7e949
  <div>
    <div class="landing-collage">
      <img @click="navigateTo('planet')" class="landing-planet" src="../../../images/moon.png" alt="">
      <img @click="navigateTo('character')" class="landing-character" src="../../../images/darth-vader.png" alt="">
      <img @click="navigateTo('starships')" class="landing-starship" src="../../../images/tie-bomber.png" alt="">
      <img @click="navigateTo('character')" class="landing-character" src="../../../images/C-3PO.png" alt="">
      <img @click="navigateTo('character')" class="landing-character" src="../../../images/luke.png" alt="">
      <img @click="navigateTo('planet')" class="landing-planet" src="../../../images/planet-dagobah.png" alt="">
      <img @click="navigateTo('starships')" class="landing-starship" src="../../../images/R2-D2.png" alt="">
      <img @click="navigateTo('character')" class="landing-character" src="../../../images/leia.png" alt="">
      <img @click="navigateTo('starships')" class="landing-starship" src="../../../images/y-wing.png" alt="">
      <img @click="navigateTo('starships')" class="landing-starship" src="../../../images/x-wing.png" alt="">
    </div>
<<<<<<< HEAD
    <Credits />
=======
    
    <Credits />

>>>>>>> e813f579c42e6e61e0147a6bbeeeb735a3d7e949
  </div>
</template>

<script>
import Credits from "./Credits";

export default {
  name: "Home",
  components: {
    Credits
  },
  data: function() {
    return {
   
    };
  },
  methods: {
    navigateTo: function(searchQuery) {
      this.$router.push({ name: "detail", params: { searchQuery: searchQuery } });
    }
  },
  created: function() {
   
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

.landing-planet,
.landing-character,
.landing-starship {
  max-width: 400px;
}

</style>


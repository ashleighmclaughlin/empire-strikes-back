<template>
  <div class="container-fullwidth">
    
  <header class=" navbar-static-top">
   <nav class="navbar navbar-light navbar-inner" id="main-nav">
   <router-link class="back" to="/"><i class="fas fa-long-arrow-alt-left"></i></router-link>
  <!-- <img class="nav-image" src="../../images/logo.png"> -->
  <form class="form-inline">
    <input v-model="searchTerm" v-on:keydown.enter.prevent="searchChanged()">
   
  </form>
</nav>

  </header>
  <div class="media-center">
    <!-- <img class="media-object" v-bind:src="detail"> -->
  </div>
  </div>
</template>

<script>
export default {
  name: "MyHeader",
  name: "Content",
  props: ["data"],
    watch: {
      data: function(val) {
        this.data=val;
      }
    },
  data: function(){
  return {
     searchTerm: ""
   
  }
},

methods: {
    searchChanged: function() {
      this.$emit("$searchChanged", this.searchTerm)
      console.log(this.searchTerm)
    }
},

};



</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
#main-nav {
 padding:20px 40px 15px 40px;
 background-color: #222;
}
 .back {
   margin-left: 60px;
 }
 form{
   margin-right: 60px;
 }
 #app {
  margin-top: 0;
 }
 i{
   color: white;
   font-size: 40px;
 }
 i:hover{
   text-shadow: 0 0 25px purple, 0 0 5px darkblue;
 }
 .nav-image{
   max-width: 100px;
   margin: 0 auto;
 }
</style>

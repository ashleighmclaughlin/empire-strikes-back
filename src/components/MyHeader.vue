<template>
  <div class="container-fullwidth">

  <header class=" navbar-static-top">
   <nav class="navbar navbar-light bg-dark navbar-inner" id="main-nav">
   <router-link class="back" to="/">Back</router-link>
 
  <form class="form-inline">
    <input v-model="searchTerm" v-on:keyup.enter="onSearch">
    <button v-on:click="detail" class="btn btn-outline-success my-2 my-sm-0" type="submit">Search</button>
  </form>
</nav>

  </header>
  <div class="media-center">
    <img class="media-object" v-bind:src="details">
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
   onSearch: function() {
      console.log("searchTerm", this.searchTerm);
    }
},

};



</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
#main-nav {
 padding:20px 40px 15px 40px;
 margin-bottom: 50px;
}
 .back {
   margin-left: 10px;
 }
 #app {
  margin-top: 0;
 }
 .media-object {
   width: 500px;
 }
</style>

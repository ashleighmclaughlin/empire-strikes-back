<template>
  <div class="container-fullwidth">

  <header class=" navbar-static-top">
   <nav class="navbar navbar-light bg-dark navbar-inner" id="main-nav">
   <router-link class="back" to="/">Back</router-link>
 
  <form class="form-inline">
    <option v-model="searchDetails" class="form-control mr-sm-2" type="text" placeholder="Search Starwars" aria-label="Search"></option>
    <button class="btn btn-outline-success my-2 my-sm-0" type="submit">Search</button>
  </form>
</nav>

 

 
  
  </header>
  </div>
</template>

<script>
export default {
  name: "MyHeader",

  data: function(){
  return {
    searchDetails: ''
  }
},
methods: {
  detailChanged: function(e) {
    this.$emit("$detailChanged", e.target.key)
  }
},
computed: {
  filteredDetails: function(){
    return this.searchDetails.filter((searchDetails) => {
      return searchDetails.title.match(this.search);
    })
  }
}
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
</style>

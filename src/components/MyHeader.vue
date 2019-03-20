<template>
  <div class="container-fullwidth">

  <header class=" navbar-static-top">
   <nav class="navbar navbar-light navbar-inner" id="main-nav">
   <router-link class="back" to="/">Back</router-link>
 
  <form class="form-inline">
    <input class="form-control mr-sm-2" type="search" placeholder="Search" aria-label="Search">
    <button class="btn btn-outline-success my-2 my-sm-0" type="submit">Search</button>
  </form>
</nav>

 

 
  
  </header>
  </div>
</template>

<script>
export default {
  name: "MyHeader"
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
#main-nav {
 padding:20px 40px 15px 40px;
 margin-bottom: 50px;
 background-color: #222;
}
 .back {
   margin-left: 10px;
 }
 #app {
  margin-top: 0;
 }
</style>

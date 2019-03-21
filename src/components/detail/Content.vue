<template>
  <div class="container">
    <img src="" alt="">
    <h2>{{ data.name }}</h2>
  </div>
</template>

<script>
  export default {
    name: "Content",
    props: ["data"],
    watch: {
      data: function(val) {
        this.data=val;
      }
    }
  }
  
  // watch the changes in the data varualve
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  
</style>
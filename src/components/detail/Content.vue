<template>
  <div class="container">
      
      <div class="row">
      <div class="col-7 ">
        <!-- <img class="item-image" :src="this.getImageURL()"> -->
        <img class="item-image" src="../../../images/placeholder.jpg">
      </div>
      <div class="col-5 item-data">
        <h2 class="item-title">{{ contentdata.name }}</h2>
        <hr>
        <div v-for="(value, key) in contentdata">
        <p>{{ key }} | {{ value }}</p>
      </div>
      </div>
      </div>

  </div>
</template>

<script>
  export default {
    name: "Content",
    props: ["contentdata"],
    watch: {
      contentdata: function(val) {
        this.contentdata=val;
      }
    },
    methods: {
      getImageURL: function(){
        return "http://localhost:8081/img/" + this.contentdata.name + ".40dff02d.png"
      }
    }
  };
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
    h2{
      color: black;
      /* text-shadow: 0 0 25px grey, 0 0 5px black; */
      font-size: 50px;
      font-family: 'Poller One', cursive;
    }
    .content{
      background-color: #222;
      background-image: url("https://www.transparenttextures.com/patterns/old-moon.png");
    }
    .item-image{
      max-width: 500px;
    }
    .item-data h2, .item-data p{
      text-align: left;
    }
    .row{
      padding: 20px;
    }
</style>
<template>
  <div>
    <MyHeader v-bind:data="data" />
    <Content v-bind:data="data" />
    <info v-bind:data="data" />
  </div>
</template>

<script>
import MyHeader from "../MyHeader"
import Content from "./Content"
import Info from "./Info"
export default {
  name: "Detail",
  components: {
    MyHeader,
    Content,
    Info


  },
  data: function() {
    return {
      data: {},
      searchQuery: ""
    }
  },
    created: function() {
    if (this.$route.params.searchQuery) {
       this.searchQuery = this.$route.params.searchQuery;
        this.$http
        .get("https://swapi.co/api/" + this.searchQuery)
        .then(function(data) {
          this.data = data;
          
        });
    }
  }
};
</script>

<style scoped></style>

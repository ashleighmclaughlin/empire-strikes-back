<template>
  <div>
    <MyHeader />
      <Content v-bind:data="data" />
  </div>
</template>

<script>
import MyHeader from "../MyHeader"

export default {
  name: "Detail",
  components: {
    MyHeader
  },
  data: function() {
    return {
      data: {},
      searchQuery: ""
    }
  },
    created: function() {
      // console.log("Hello");
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

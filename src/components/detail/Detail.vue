<template>
  <div>
    <MyHeader />
      <Content />
      <Info data="data" />
      <MyFooter />
  </div>
</template>

<script>
import MyHeader from "../MyHeader"
import Content from "./Content";
import Info from "./Info";
import MyFooter from "../MyFooter";

export default {
  name: "Detail",
  props: ["data"],
  data: function(){
    return{
      data: {},
      searchQuery: "",
    }
  }, 
  components: {
    MyHeader,
    Content,
    Info,
    MyFooter,
    },
    created: function() {      
      if (this.$route.params.searchQuery) {
        this.searchQuery = this.$route.params.searchQuery;}
        this.$http
          .get("https://swapi.co/api" + data)
          .then(function(data) {
            this.data = data;
          });
  }
}
</script>

<style scoped> 

</style>

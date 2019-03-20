<template>
  <div>
    <MyHeader />
       <Planet v-if="type === 'planet'"  />
      <Character v-if="type === 'character'"  />
       <Starships v-if="type === 'starships'"  />
        <Details v-if="type === 'details'"  />
  
   
      <Content />
      <Info />
      <MyFooter/>
  </div>
</template>

<script>
import MyHeader from "../MyHeader"

export default {
  name: "Detail",
  data: function() {
    return {
      searchQuery: '',
    };
  },
  components: {
    MyHeader

  },
    created: function() {
    if (this.$route.params.searchQuery) {
       this.searchQuery = this.$route.params.searchQuery;
    }
  }

};
</script>

<style scoped></style>

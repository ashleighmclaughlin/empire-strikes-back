<template>
  <div class="container">
    <div>
      <p>
          Name: {{ data.name }}
      </p>
    </div>
  </div>
</template>

<script>
export default {
  name: "Info",
  props: ["data"],
  watch: {
    data: function(val) {
      this.data=val;
    }
  }
};
</script>


<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped></style>

<template>
  <div class="container">
    <div>
      <p>
          {{ data.name }}
      </p>
    </div>
  </div>
</template>

<script>
export default {
  name: "Info",
  props: ["data"]
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped></style>

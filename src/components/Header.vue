<template>
  <div class="header">
    <h1>DECAP Database Editor</h1>
    <img alt="USGS logo" src="../assets/usgs_logo.svg" id="usgs-logo">
  </div>
</template>

<script>
export default {
  name: "Header",
  props: {
    msg: String,
    hover: String,
    seen: Boolean
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1 {
  font-size: 5em;
}

.header {
  background-color: darkgray;
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 2ch;
}
</style>

<template>
  <div id="app">
    <h2>Mouse position:</h2>
    <p>Mouse position X: {{ mousePosX }}</p>
    <p>Mouse position Y: {{ mousePosY }}</p>
  </div>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      mousePosX: 0,
      mousePosY: 0,
    };
  },
  mounted() {
    document.addEventListener("mousemove", (event) => {
      this.mousePosX = event.clientX;
      this.mousePosY = event.clientY;
    });
  },
};
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #000000;
  margin: 60px;
}
</style>

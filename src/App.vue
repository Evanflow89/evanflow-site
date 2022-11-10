<template>
  <div id="app">
    <BaseMain />
  </div>
</template>

<script>
import "bootstrap/dist/css/bootstrap.min.css";
import "bootstrap";
import BaseMain from "./components/BaseMain.vue";
export default {
  name: "App",
  components: {
    BaseMain,
  },
};
</script>

<style lang="scss">
@import "./assets/style/global.scss";
</style>

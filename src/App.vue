<template>
  <div id="app">
    <BaseHeader />
  </div>
</template>

<script>
import "bootstrap/dist/css/bootstrap.min.css";
import "bootstrap";
import BaseHeader from "./components/BaseHeader.vue";
export default {
  name: "App",
  components: {
    BaseHeader,
  },
};
</script>

<style lang="scss">
@import "./assets/style/global.scss";
</style>

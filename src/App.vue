<template>
  <div id="app">
    <BaseHeader />
    <BaseMain />
  </div>
</template>

<script>
import "bootstrap/dist/css/bootstrap.min.css";
import "bootstrap";
import BaseHeader from "./components/BaseHeader.vue";
import BaseMain from "./components/BaseMain.vue";
export default {
  name: "App",
  components: {
    BaseHeader,
    BaseMain,
  },
};
</script>

<style lang="scss">
@import "./assets/style/global.scss";
</style>

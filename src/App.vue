<template>
  <div id="app">
    <BaseMain />
    <BaseFooter />
  </div>
</template>

<script>
import "bootstrap/dist/css/bootstrap.min.css";
import "bootstrap";
import BaseMain from "./components/BaseMain.vue";
import BaseFooter from "./components/BaseFooter.vue";
export default {
  name: "App",
  components: {
    BaseMain,
    BaseFooter,
  },
  mounted: function () {
    this.$nextTick(function () {});
  },
};
</script>

<style lang="scss">
@import "./assets/style/global.scss";
#hideAll {
  position: fixed;
  left: 0px;
  right: 0px;
  top: 0px;
  bottom: 0px;
  background-color: white;
  z-index: 99; /* Higher than anything else in the document */
}
</style>

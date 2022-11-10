<template>
  <header>
    <h1 class="text-center">Mishima Dev</h1>
  </header>
</template>

<script>
export default {
  name: "BaseHeader",
};
</script>

<style lang="scss" scoped>
header {
  font-family: "Nanum Myeongjo", serif;
  font-size: 1rem;
  background: linear-gradient(to left top, #05bfd6, #202328);
  // background-image: url("../assets/img/head.jpg");
  // // background-position: center;
  // // background-size: cover;
  h1 {
    color: white;
  }
}
</style>
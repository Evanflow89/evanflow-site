<template>
  <main>
    <TopMain />
    <MiddleMain />
  </main>
</template>

<script>
import TopMain from "../section/TopMain.vue";
import MiddleMain from "../section/MiddleMain.vue";
export default {
  name: "BaseMain",
  components: {
    TopMain,
    MiddleMain,
  },
};
</script>

<style lang="scss">
</style>
<template>
  <main>
    <TopMain />
    <MiddleMain />
    <BottomMain />
  </main>
</template>

<script>
import TopMain from "../section/TopMain.vue";
import MiddleMain from "../section/MiddleMain.vue";
import BottomMain from "../section/BottomMain.vue";
export default {
  name: "BaseMain",
  components: {
    TopMain,
    MiddleMain,
    BottomMain,
  },
};
</script>

<style lang="scss">
</style>
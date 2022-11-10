<template>
  <main>
    <TopMain />
    <BottomMain />
  </main>
</template>

<script>
import TopMain from "../section/TopMain.vue";
import BottomMain from "../section/BottomMain.vue";
export default {
  name: "BaseMain",
  components: {
    TopMain,
    BottomMain,
  },
};
</script>

<style lang="scss">
</style>
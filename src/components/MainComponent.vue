<template>
  <main>
    <main-grid />
  </main>
</template>

<script>
import MainGrid from "./MainGrid.vue";

export default {
  name: "MainComponent",
  components: {
    MainGrid,
  },
};
</script>

<style scoped lang="scss">
@import "@/assets/styles/vars.scss";
main {
  width: 100%;
  // height: 800px;
  display: flex;
  justify-content: space-around;
  align-content: center;
  background-color: $bg-color;
}
</style>
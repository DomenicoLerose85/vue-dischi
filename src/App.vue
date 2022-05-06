<template>
  <div id="app">
    <header-component />
    <main-component />
    <main-grid />
  </div>
</template>


<script>
import HeaderComponent from "./components/HeaderComponent.vue";
import MainComponent from "./components/MainComponent.vue";
import MainGrid from "./components/MainGrid.vue";

export default {
  name: "App",
  components: {
    HeaderComponent,
    MainComponent,
    MainGrid,
  },
};
</script>

<style lang="scss">
@import "@/assets/styles/general.scss";
</style>

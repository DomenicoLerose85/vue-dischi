<template>
  <div id="app">
    <header-component />
    <main-component />
  </div>
</template>


<script>
import HeaderComponent from "./components/HeaderComponent.vue";
import MainComponent from "./components/MainComponent.vue";

export default {
  name: "App",
  components: {
    HeaderComponent,
    MainComponent,
  },
};
</script>

<style lang="scss">
@import "@/assets/styles/general.scss";
</style>

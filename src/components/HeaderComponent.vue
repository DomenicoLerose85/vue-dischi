<template>
  <header>
    <img src="../assets/img/logo-small.svg" alt="logo" />
  </header>
</template>

<script>
export default {
  name: "HeaderComponent",
  props: [],
};
</script>

<style scoped lang="scss">
header {
  width: 100%;
  height: 60px;
  background-color: #2e3a46;
}

img {
  width: 30px;
  height: 30px;
  margin-top: 15px;
  margin-left: 30px;
}
</style>

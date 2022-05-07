<template>
  <div>
    <div v-for="(item, index) in discList" :key="item.id">
      id {{ item.id }} poster{{ item.poster }} title{{ item.title }} author{{
        item.author
      }}
    </div>
  </div>
</template>

<script>
import axios from "axios";

export default {
  name: "MainGrid",
  data() {
    return {
      discList: [],
      endPoint: "https://flynn.boolean.careers/exercises/api/array/",
    };
  },
  mounted() {
    axios.get(this.endPoint + "music").then((res) => {
      console.log(res);
      this.discList = res.data;
    });
  },
};
</script>

<style scoped lang="scss">
</style>
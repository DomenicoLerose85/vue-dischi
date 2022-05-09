<template>
  <div>
    <div v-for="item in discList" :key="item.id">
      id {{ item.id }} poster{{ item.poster }} title{{ item.title }} author{{
        item.author
      }}
      genre {{ item.genre }}
      <img :src="item.image" :alt="item.name" />
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
    axios
      .get(this.endPoint + "music")
      .then((res) => {
        console.log(res);
        this.discList = res.data.response;
      })
      .catch((error) => {
        console.log(error);
      });
  },
};
</script>

<style scoped lang="scss">
</style>
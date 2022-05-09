<template>
  <div>
    <div class="container" v-for="item in discList" :key="item.id">
      <!-- <div v-for="item in discList" :key="item.id">
      genre {{ item.genre }} -->
      <div class="row row-cols-5 justify-content-evenly align-items-center">
        <div class="card-container">
          <img :src="item.poster" :alt="item.name" />
          <h2>{{ item.title }}</h2>
          <h3>{{ item.author }}</h3>
        </div>
      </div>
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
.container {
  display: flex;
  justify-content: space-around;
  align-content: center;
}

.card-container {
  width: 150px;
  height: 200px;
  background-color: #2e3a46;
  border-radius: 5px;
  margin-right: 10px;
}

img {
  width: 80px;
  height: 80px;
  margin-top: 15px;
  margin-left: 25px;
}

h2 {
  text-align: center;
  color: white;
  font-weight: bold;
  margin-top: 10px;
  font-size: 10px;
  font-size: 18px;
}

h3 {
  text-align: center;
  color: #656f73;
  font-size: 15px;
}
</style>
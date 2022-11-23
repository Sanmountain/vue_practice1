<template>
  <div id="app">
    <div class="menu">
      <a v-for="a in menus" :key="a">{{ a }}</a>
    </div>

    <div class="black-bg" v-if="modalOpen == true">
      <div class="white-bg">
        <h4>상세페이지임</h4>
        <p>상세페이지 내용임</p>
        <button @click="modalOpen = false">닫기</button>
      </div>
    </div>

    <div>
      <img :src="onerooms[0].image" class="room_img" />
      <h4 @click="modalOpen = true">{{ onerooms[0].title }}</h4>
      <p>{{ onerooms[0].price }}</p>
    </div>
    <div>
      <img :src="onerooms[1].image" class="room_img" />
      <h4 @click="modalOpen = true">{{ onerooms[1].title }}</h4>
      <p>{{ onerooms[1].price }}</p>
    </div>
    <div>
      <img :src="onerooms[2].image" class="room_img" />
      <h4 @click="modalOpen = true">{{ onerooms[2].title }}</h4>
      <p>{{ onerooms[2].price }}</p>
    </div>
    <div>
      <img :src="onerooms[3].image" class="room_img" />
      <h4 @click="modalOpen = true">{{ onerooms[3].title }}</h4>
      <p>{{ onerooms[3].price }}</p>
    </div>
    <div>
      <img :src="onerooms[4].image" class="room_img" />
      <h4 @click="modalOpen = true">{{ onerooms[4].title }}</h4>
      <p>{{ onerooms[4].price }}</p>
    </div>
    <div>
      <img :src="onerooms[5].image" class="room_img" />
      <h4 @click="modalOpen = true">{{ onerooms[5].title }}</h4>
      <p>{{ onerooms[5].price }}</p>
    </div>
  </div>
</template>

<script>
import data from "./oneroom.js";

export default {
  name: "App",
  data() {
    return {
      onerooms: data,
      modalOpen: false,
      신고수1: 0,
      신고수2: 0,
      신고수3: 0,
      menus: ["Home", "Shop", "About"],
      products: ["역삼동원룸", "천호동원룸", "마포구원룸"],
    };
  },
  components: {},
};
</script>

<style>
body {
  margin: 0;
}
div {
  box-sizing: border-box;
}
.black-bg {
  width: 100%;
  height: 100%;
  background: rgba(0, 0, 0, 0.5);
  position: fixed;
  padding: 20px;
}
.white-bg {
  width: 100%;
  background: white;
  border-radius: 8px;
  padding: 20px;
}
.room_img {
  width: 100%;
  margin-top: 40px;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

.menu {
  background: darkslateblue;
  padding: 15px;
  border-radius: 5px;
}
.menu a {
  color: white;
  padding: 10px;
}
</style>

<template>
  
  <div class="black-bg" v-if="opened == true">
    <div class="white-bg">
      <h4>상세페이지임</h4>
      <p>상세페이지 내용임</p>
      <button @click="opened=false">닫기</button>
    </div>
  </div>
  
  <div class="menu">
    <a v-for="menubar in menus" :key="menubar">{{menubar}}</a>
  </div>



  <div v-for="(item, index) in items" :key="index">
    <img :src="items[index].image" class="room-img">
    <h4>{{items[index].title}}</h4>
    <p>{{items[index].price}}원</p>
  </div>

</template>

<script>

import data from './assets/data.js'

export default {
  name: 'App',
  data () {
    return{
      items : data,
      opened : false,
      count : [0,0,0],
      products : ['역삼동 원룸','천호동 원룸','마포구 원룸'],
      costs : ['50만원','60만원','70만원'],
      menus : ['Home','Shop','About'],
    }
  },
  methods: {
    increase(i){
      this.count[i]++;
    },
  },
  components: {
  }
}
</script>

<style>
body {
  margin: 0;
}
div {
  box-sizing: border-box;
}
.black-bg{
  width: 100%; height: 100%;
  background: rgba(0,0,0,0.5);
  position: fixed; padding: 20px;
}

.white-bg{
  width: 100%;
  background: white;
  border-radius: 8px; padding: 20px;
}

.room-img{
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
.menu a{
  color: white;
  padding: 10px;
}


</style>

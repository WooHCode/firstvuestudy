<template>
  <div class="menu">
    <a v-for="menubar in menus" :key="menubar">{{menubar}}</a>
  </div>

  <div>
    <img src="./assets/room0.jpg" class="room-img">
    <h4>{{products[0]}}</h4>
    <p>50만원</p>
    <button @click="increase(0)">허위매물신고</button> <span>신고수 : {{count[0]}}</span>
  </div>

  <div>
    <img src="./assets/room1.jpg" class="room-img">
    <h4>{{products[1]}}</h4>
    <p>60만원</p>
    <button @click="increase(1)">허위매물신고</button> <span>신고수 : {{count[1]}}</span>
  </div>

  <div>
    <img src="./assets/room2.jpg" class="room-img">
    <h4>{{products[2]}}</h4>
    <p>70만원</p>
    <button @click="increase(2)">허위매물신고</button> <span>신고수 : {{count[2]}}</span>
  </div>
</template>

<script>



export default {
  name: 'App',
  data () {
    return{
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

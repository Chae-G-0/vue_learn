<template>

  <div class="black_bg" v-if="open == true">
    <div class="white_bg">
      <h2>상세페이지</h2>
      <p>상세페이지 내용</p>
      <button @click="open = false">닫기</button>
    </div>
  </div>


  <div class="menu">
    <a v-for="작명 in menus" :key="작명"> {{작명}} </a>
  </div>
  <div>
    <h3 @click="open = true"> {{ products[0].title }} </h3>
    <p>{{products[0].price}}</p>
    <button @click="count[0]++">허위매물신고</button>
    <span>신고수 : {{ count[0] }}</span>
  </div>
  <div>
    <h3>{{ products[1].title }} </h3>
    <p>1000/150</p>
    <button @click="count[1]++">허위매물신고</button>
    <span>신고수 : {{ count[1] }}</span>
  </div>
  <div>
    <h3>{{ products[2].title }} </h3>
    <p>1000/50</p>
    <button @click="count[2]++">허위매물신고</button>
    <span>신고수 : {{ count[2] }}</span>
  </div>
</template>

<script>
import data from './data'

export default {
  name: 'App',
  data() {
    return {
      open: false,
      count: [0, 0, 0],
      menus: ['Home', 'Shop', 'About'],
      products : data,
    }
  },
  methods: {
    increase() {
      this.count++
    },
  },
}
</script>

<style>
body {
    margin: 0;
  }
div {
    box-sizing: border-box;
  }
.black_bg {
    width: 100%;
    height: 100%;
    background: rgba(0, 0, 0, 0.5);
    position: fixed;
    padding: 20px;
  }
.white_bg {
    width: 100%;
    background: #fff;
    border-radius: 8px;
    padding: 20px;    
  } 
h3 {
  cursor: pointer;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

.menu {
  background: #7943ca;
  padding: 15px;
  border-radius: 5px;
}

.menu a {
  color: #fff;
  padding: 10px;
}
</style>

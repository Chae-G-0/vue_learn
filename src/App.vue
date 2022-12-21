<template>
  <div class="menu">
    <a v-for="작명 in menus" :key="작명"> {{작명}} </a>
  </div>
  <div>
    <h3> {{products[0]}} </h3>
    <p>500/50</p>
  </div>
  <div>
    <h3>{{products[1]}} </h3>
    <p>1000/150</p>
  </div>
  <div>
    <h3>{{products[2]}} </h3>
    <p>1000/50</p>
  </div>
</template>

<script>

export default {
  name: 'App',
  data() {
    return {
      menus: ['Home', 'Shop', 'About'],
      products : ['서면 원룸', '해운대 원룸', '부산대 원룸']
    }
  }
}
</script>

<style>
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

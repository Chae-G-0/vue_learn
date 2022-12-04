<template>
  <img alt="Vue logo" src="./assets/logo.png">
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
  margin-top: 60px;
}
</style>

<template>
  <div id="app">
    <img src="./assets/logo.png" @click="getData">
    <router-view></router-view>
  </div>
</template>

<script>
export default {
  name: 'app',
  methods: {
    getData: function () {
      this.$http.get('/api/topics').then(res => {
        console.log(res.body)
      }, err => {
        console.log(err.body)
      })
    }
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>

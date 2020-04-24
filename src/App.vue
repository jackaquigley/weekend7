<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <HelloWorld msg="Welcome to Your Vue.js App"/>
  </div>
</template>

<script>

export default {
  name: 'app',
  data() {
    return {
      stats: [],
    }
  },
    mounted(){
      fetch('https://api.covid19uk.live/')
      .then(res => res.json())
      .then(data => this.stats = data)
      .then(sortData())
    },
    methods: {
      sortData: function(){
      const data = stats.splice
      const info = stats.splice
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

<template>
  <div id="app">
    <img v-if="show" v-on:click="reverse" src="./assets/logo.png">
    <router-view/>
    <button v-on:click="reverse">Reverse</button>
  </div>
</template>

<script>
export default {
  name: 'App',
  data () {
    return {
      show: true
    }
  },
  methods: {
    reverse () {
      this.show = !this.show
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

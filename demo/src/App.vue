<template>
  <div id="app">
    <img src="./assets/logo.png">
    <announcer :text="announcement"></announcer>  
    <button v-on:click="announce">Trigger a new announcement</button>
  </div>
</template>

<script>

import Announcer from './announcer.vue'

export default {
  name: 'app',
  components: {
    Announcer
  },
  methods: {
    announce: function (event) {
      this.announcement = 'Here\'s a new annoucement!'
      setTimeout(() => {
        this.announcement = ''
      }, 2000)
    }
  },
  data: function () {
    return {
      announcement: ''
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

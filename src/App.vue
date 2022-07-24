<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <HelloWorld msg="Welcome to Your Vue.js App"/>
    <vue-telegram-login
        mode="callback"
        telegram-login="tresGoldTestBot"
        @callback="yourCallbackFunction"
    />
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import { vueTelegramLogin } from 'vue-telegram-login'

export default {
  name: 'App',
  components: {
    HelloWorld, vueTelegramLogin
  },
  methods:{
    yourCallbackFunction (e) {
      console.log(e)
    },
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

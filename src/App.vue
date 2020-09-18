<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <vue-webrtc ref="webrtc" width="100%" roomId="sample-room"/>
    Room: sample-room
    </div>
</template>

<script>
// import HelloWorld from './components/HelloWorld.vue'
import Vue from 'vue'
import WebRTC from 'vue-webrtc'

import * as io from 'socket.io-client'
window.io = io

Vue.use(WebRTC)
// or
// import {WebRTC} from 'vue-webrtc'
// Vue.component(WebRTC.name, WebRTC)
export default {
  name: 'App',
  mounted: function () {
    this.$refs.webrtc.join()
  },
  components: {
    // HelloWorld
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

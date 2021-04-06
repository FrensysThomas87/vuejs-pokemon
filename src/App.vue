<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <BasicComponent v-for="(name, i) in usernames" :name="name" :key="i"/>
    <HelloWorld msg="Welcome to Your Vue.js App"/>
    
  </div>
 
</template>

<script>
import BasicComponent from './components/BasicComponent.vue'
import HelloWorld from './components/HelloWorld.vue'

export default {
  name: 'App',
  components: {
    HelloWorld,
    BasicComponent
  },

  data: function(){
    return{
      usernames: ['pippo', 'pluto', 'paperino']
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

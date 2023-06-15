<template>
  <h1 v-if="welcome">Welcome to the battle program.</h1>
  <h3 v-if="welcome">To get started, start by filling out this form</h3>
<registration/>
</template>

<script>
import registration from './components/registration.vue'
export default {
  name: 'App',
  components: {
    registration 
  },
  data(){
    return{
      welcome: true,
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

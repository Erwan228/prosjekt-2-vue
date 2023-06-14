<template>
  <h1 v-if="welcome">Welcome to... the program</h1>
  <h2 v-if="welcome">We don't have a name for it yet...fuck</h2>
  <h3 v-if="welcome">Anyways, start by filling out this form</h3>
<registration/>
<p>{{ name }}</p>
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

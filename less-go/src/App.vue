<template>
  <h1 v-if="welcome">Welcome to the battle program.</h1>
  <h3 v-if="welcome">To get started, start by filling out this form</h3>
<registration @saveData="makeFinal"/>
<button @click="doIt">Come on pls</button>
<p v-if="final">{{ name }} {{ age }} {{ gender }} {{ race }} {{ magic }} {{ weapon }} {{ motivation }}</p>
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
      name: '',
      age: null,
      gender: '',
      race: '',
      magic: '',
      weapon: '',
      motivation: '',
      final: false,
    }
  },
  methods: {
    doIt(){
      console.log(this.name)
      console.log(this.age)
      console.log(this.gender)
      console.log(this.race)
      console.log(this.magic)
      console.log(this.weapon)
      console.log(this.motivation)
      this.final = true
    },
    makeFinal(Name, Age, Gender, Race, Magic, Weapon, Motivation){
      this.name = Name
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
.lessGo {
  background: #0b6dff;
    border: 0;
    padding: 10px 20px;
    margin-top: 20px;
    color: white;
    border-radius: 20px;
}
</style>

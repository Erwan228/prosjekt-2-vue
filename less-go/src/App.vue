<template>
  <h1 v-if="welcome">Welcome to the battle program.</h1>
  <h3 v-if="welcome">To get started, start by filling out this form</h3>
  <registration @saveData="makeFinal"/>
  <h3 v-if="submitted">Wonderful, now we will review your info by pressing the button below</h3>
  <button @click="doIt">Come on pls</button>
  <p id="allInfoen" v-if="final">Name: {{ name }}, Age: {{ age }}, Gender: {{ gender }}, Race: {{ race }}, Magic: {{ magic }}, Weapon: {{ weapon }}, Motivation: {{ motivation }}</p>
  <button v-if="final" @click="newTest">New thing</button>
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
      submitted: false,
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
      this.age = Age
      this.gender = Gender
      this.race = Race
      this.magic = Magic
      this.weapon = Weapon
      this.motivation = Motivation
      this.submitted = true
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
button{
  position: center;
    background: #0ad696;
    border: 0;
    padding: 10px 20px;
    margin-top: 0px;
    color: white;
    border-radius: 20px;
}
</style>

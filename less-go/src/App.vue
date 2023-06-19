<template>
  <Modal v-if="notPermitted"/>
  <h1 v-if="welcome">Welcome to the battle program.</h1>
  <h3 v-if="welcome">To get started, start by filling out this form</h3>
  <registration @saveData="makeFinal"/>
  <h3 v-if="submitted">Wonderful, now we will review your info by pressing the button below</h3>
  <button @click="doIt">Come on pls</button>
  <p id="allInfoen" v-if="final">Name: {{ name }}, Age: {{ age }}, Gender: {{ gender }}, Race: {{ race }}, Magic: {{ magic }}, Weapon: {{ weapon }}, Motivation: {{ motivation }}</p>
  <button v-if="final" @click="getAllInfo">Hent ut infoen</button>
</template>

<script>
import Modal from './components/modal.vue'
import registration from './components/registration.vue'
export default {
  name: 'App',
  components: {
    registration,
    Modal,
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
      notPermitted: false,
    }
  },
  methods: {
    makeFinal(Name, Age, Gender, Race, Magic, Weapon, Motivation){ /*sjekker om karakter er gammel nok*/
      if(Age < 18){
        this.welcome = false
        this.final = false
        this.submitted = false
        this.notPermitted = true
      }
      else{
      this.name = Name
      this.age = Age
      this.gender = Gender
      this.race = Race
      this.magic = Magic
      this.weapon = Weapon
      this.motivation = Motivation
      this.submitted = true
      }
    },
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
    getAllInfo(){
      console.log(document.getElementById('allInfoen').innerHTML)
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

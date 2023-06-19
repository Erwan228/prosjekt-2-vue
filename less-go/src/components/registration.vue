<template>
 <form>
    <label>Name:</label>
    <input type="text" required v-model="Name" spellcheck="false">

    <label>Age:</label>
    <input type="number" min="18" required v-model="Age">

    <label>Gender:</label>
    <select v-model="Gender" required>
            <option value="Male" style="background: blue; color: whitesmoke">Male</option>
            <option value="Non-binary" style="background: purple; color: white;">Non-binary</option>
            <option value="Female" style="background: red;">Female</option>
        </select>

    <label>Race:</label>
    <input type="text" required v-model="Race" spellcheck="false">
    
    <label>Magic:</label>
    <input type="text" required v-model="Magic" spellcheck="false">

    <label>Weapon:</label>
    <input type="text" required v-model="Weapon" spellcheck="false">

    <label>Motivation:</label>
    <input type="text" required v-model="Motivation" spellcheck="false">

    <button @click.prevent="$emit('saveData', this.Name, this.Age, this.Gender, this.Race, this.Magic, this.Weapon, this.Motivation)" @click="log">Submit</button>
 </form>

</template>

<script>
export default{
    data(){
        return{
            Name: '',
            Age: 18,
            Gender: '',
            Race: '',
            Magic: '',
            Weapon: '',
            Motivation: '',
        }
    },
    methods: {
        log(){
            console.log(this.Name)
            console.log(this.Age)
            console.log(this.Gender)
            console.log(this.Race)
            console.log(this.Magic)
            console.log(this.Weapon)
            console.log(this.Motivation)
        }
    }
}
</script>

<style scoped>
form {
    max-width: 420px;
    margin: 30px auto;
    background: white;
    text-align: left;
    padding: 40px;
    border-radius: 10px;
}
label {
    color: #aaa;
    display: inline-block;
    margin: 25px 0 15px;
    font-size: 0.6em;
    text-transform: uppercase;
    letter-spacing: 1px;
    font-weight: bold;
}
input, select {
    display: block;
    padding: 10px 6px;
    width: 100%;
    box-sizing: border-box;
    border: none;
    border-bottom: 1px solid #ddd;
    color: #555;
}
input[type="checkbox"]{
    display: inline-block;
    width: 16px;
    margin: 0 10px 0 0;
    position: relative;
    top: 2px;
}

button{
    position: center;
    background: #0b6dff;
    border: 0;
    padding: 10px 20px;
    margin-top: 20px;
    color: white;
    border-radius: 20px;
}
</style>
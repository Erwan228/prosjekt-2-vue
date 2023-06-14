<template>
 <form>
    <label>Name:</label>
    <input type="text" required :name="name" spellcheck="false">

    <label>Age:</label>
    <input type="number" min="18" required :age="age">

    <label>Gender:</label>
    <select :gender="gender">
            <option value="Male" style="background: blue; color: whitesmoke">Male</option>
            <option value="Non-binary" style="background: purple; color: white;">Non-binary</option>
            <option value="Female" style="background: red;">Female</option>
        </select>

    <label>Weapon:</label>
    <input type="text" required :weapon="weapon" spellcheck="false">

    <label>Magic:</label>
    <input type="text" required :magic="magic" spellcheck="false">

    <label>Race:</label>
    <input type="text" required :race="race" spellcheck="false">

    <label>Motivation:</label>
    <input type="text" required :motivation="motivation" spellcheck="false">
 </form>
</template>

<script>
export default{
    data(){
        return{
            name: '',
            age: '',
            gender: '',
            weapon: '',
            magic: '',
            race: '',
            motivation: '',
        }
    },
    props: ['name', 'age', 'gender', 'weapon', 'magic', 'race', 'motivation']
}
</script>

<style>
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
</style>
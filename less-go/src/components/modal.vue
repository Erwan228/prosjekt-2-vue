<template>
    <div class="backdrop">
        <div class="modal">
            <h2>THE PARTICIPANT IS NOT OLD ENOUGH</h2>
            <h3>COME BACK WHEN THEY ARE OLD ENOUGH</h3>
        </div>
    </div>
</template>

<script>
export default{}
</script>

<style scoped>
h2{
    color: black
}
h3{
    color: black
}
.modal{
    width: 400px;
    padding: 20px;
    margin: 100px auto;
    background: red;
    border-radius: 10px;
}
.backdrop{
    top: 0;
    position: fixed;
    background: rgba(255, 0, 0, 0.4);
    width: 100%;
    height: 100%;
}
</style>
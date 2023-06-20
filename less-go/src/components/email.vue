<template>
    <form action="mailto:erwan.stephane.beaudoin.005@gmail.com" method="get" enctype="text/plain">
    Subject:<br>
    <input type="text" name="subject" value="Fighter"><br>
    Message:<br>
    <textarea name="body" rows="5" cols="30" spellcheck="false">{{ infoenTilEmail }}</textarea><br>
    <input type="submit" value="Send">
    </form>
</template>

<script>
export default{
    props: ['infoenTilEmail']
    }

</script>

<style scoped>
form {
    max-width: 420px;
    margin: 30px auto;
    
    padding: 40px;
    border-radius: 10px;
}
</style>
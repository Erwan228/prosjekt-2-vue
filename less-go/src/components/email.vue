<template>
    <form action="mailto:erwan.stephane.beaudoin.005@gmail.com" method="get" enctype="text/plain">
    Subject:<br>
    <input type="text" name="subject" value="Fighter"><br>
    Message:<br>
    <textarea name="body" rows="5" cols="30" >{{ infoenTilEmail }}</textarea><br>
    <input type="submit" value="Send">
    </form>
</template>

<script>
export default{
    props: ['infoenTilEmail']
    }

</script>

<style>

</style>
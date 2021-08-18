<template>
    <div class="joke">{{joke}}</div>
</template>

<script>
export default {
    props:["joke"]
}
</script>

<style>
.joke{
    border:3px solid black;
    border-radius: 10px;
    margin: 10px 0;
    padding:10px;
    font-size: 1.5rem;
}
</style>
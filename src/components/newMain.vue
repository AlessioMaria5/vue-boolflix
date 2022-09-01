<template>
<div class="myMain">
    <ul>
        <li v-for="(film,index) in displayMyFilms" :key="index">
        {{film.original_title}}</li>
    </ul>
</div>
</template>

<script>
export default {
    name: 'NewMain',
    props: {
        displayMyFilms:Array
    } 
}
</script>

<style lang="scss">

.myMain {
    
    color: black;
    text-align: center;
}
</style>
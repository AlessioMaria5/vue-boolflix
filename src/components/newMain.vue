<template>
<div class="myMain">
    <ul>
        <li v-for="(film,index) in displayMyFilms" :key="index">
        <p>{{film.original_title}}</p>
        <p>{{film.title}}</p>
        <p>{{film.original_language}}</p>
        <p>{{film.vote_average}}</p>
    </li>
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
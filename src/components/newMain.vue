<template>
<div class="myMain">
    <h1>FILMs</h1>
    <ul>
        <li v-for="(film,index) in displayMyFilms" :key="index">
            <img :src="'https://image.tmdb.org/t/p/w500/'+film.backdrop_path" alt="">
            <p>{{film.original_title}}</p>
            <p>{{film.title}}</p>
            <img class="myFlag" :src="film.original_language"/>
            <p>{{film.original_language==false?'displayOff':''}}</p>
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
        
        ul {
            display:flex;
            background-color: black;
            overflow: auto;
            color:white;
            li{
                
            }
        }
}

.displayOff {
    display: none;
}

.myFlag {
    width: 25px;
    
}
</style>
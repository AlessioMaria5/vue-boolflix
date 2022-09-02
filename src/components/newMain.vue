<template>
<div class="myMain">
    <h1>FILMs</h1>
    <ul>
        <li v-for="(film,index) in displayMyFilms" :key="index">
            <div class="myCopertina">
                <img :src="'https://image.tmdb.org/t/p/w500/'+film.backdrop_path" alt="">

                <div class="contenuti">
                    <p>{{'Original Title: ' + film.original_title}}</p>
                    <p>{{'Title: '+film.title}}</p>

                    <div class="lng">
                        <span>lng: </span><img class="myFlag" :src="film.original_language"/>
                    </div>

                    <p>{{'VOTO: '+film.vote_average}}</p>
                    <p>{{'Description: '+film.overview}}</p>
                </div>

            </div>
           
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
               list-style: none; 
            }
        }
}

.displayOff {
    display: none;
}

.myFlag {
    width: 25px;
    
}

.myCopertina {

    position:relative;
    height: 230px;
    
    ul {

        list-style:none;
    }

    .contenuti {
       
        position: absolute;
        margin-left: auto;
        margin-right: auto;
        left: 0;
        right: 0;
        top: 0;
        padding: 10px;
        overflow-y:scroll;
        height: 100%;
        z-index: 0;
    
}
}

.myCopertina img {
    position:relative;
    object-fit: cover;
    z-index: 1;
}
.myCopertina img:hover {
    opacity: 0;
    
    }

.contenuti:hover {

    display:block;
    line-height:100%;
}
</style>
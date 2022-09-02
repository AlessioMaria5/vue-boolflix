<template>
  <div class="TVseries">
      TV SERIES
      <ul>
        <li v-for="(TVserie, index) in displayMySeries" :key="index">
        <img :src="'https://image.tmdb.org/t/p/w500/'+TVserie.backdrop_path" alt="">
        <p>{{TVserie.original_name}}</p>
        <p>{{TVserie.name}}</p>
        <img class="myFlag" :src="TVserie.original_language"/>
        <p>{{TVserie.vote_average}}</p>
    </li>
       
      </ul>
  </div>
</template>

<script>
export default {
    name: 'TVseries',
    props: {
        displayMySeries:Array
    }
}
</script>

<style lang="scss">

ul {
            display:flex;
            background-color: black;
            overflow: auto;
            color:white;
            text-align: center;
            li{
                
            }
        }

.myFlag {
    width: 25px;
    
}

</style>
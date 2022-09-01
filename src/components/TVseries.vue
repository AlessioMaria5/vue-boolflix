<template>
  <div class="TVseries">
      TV SERIES
      <ul>
          <li v-for="(TVserie, index) in displayMySeries" :key="index">
        <p>{{TVserie.original_title}}</p>
        <p>{{TVserie.title}}</p>
        <img class="myFlag" :src="TVserie.original_language"/>
        <p>{{TVserie.original_language==false?'displayOff':''}}</p>
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

.myFlag {
    width: 25px;
    
}

</style>
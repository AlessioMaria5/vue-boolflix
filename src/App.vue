<template>
  <div id="app">
    <NewHeader @search="findFilm"/>
    <NewMain />
  </div>
</template>

<script>
import NewHeader from "./components/newHeader.vue";
import NewMain from "./components/newMain.vue";
import axios from 'axios';

export default {
  name: 'App',
  components: {
    NewHeader,
    NewMain
},
  data(){

  },
  methods: {
  
  findFilm(mySearch){
    axios.get('https://api.themoviedb.org/3/search/movie?api_key=99a17c4a907152d283c8225f68325acb&query='+ mySearch)
    .then((res)=> {
      console.log(res)
    })
    
  }
}

}


</script>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;

}
</style>

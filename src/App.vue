<template>
  <div id="app">
    <NewHeader @search="searching" />
    <NewMain />
  </div>
</template>

<script>
import NewHeader from "./components/newHeader.vue";
import NewMain from "./components/newMain.vue";

export default {
  name: 'App',
  components: {
    NewHeader,
    NewMain
},
  data(){

  }
}
</script>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;

}
</style>

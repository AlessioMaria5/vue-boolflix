<template>
  <div class="TVseries">
      TV SERIES
      <ul>
          <li v-for="(TVserie, index) in displayMySeries" :key="index">
        {{TVserie.original_title}}</li>
       
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

<style>

</style>
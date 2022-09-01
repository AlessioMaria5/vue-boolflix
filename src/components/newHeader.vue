<template>
<div class="myHeadContainer">
    <input v-model="filmSearch" id="filmSearch" type="text">
    <button @click="$emit('search', filmSearch )" class="mySrcBtn">Search</button>
</div>
</template>

<script>
export default {
    name: "newHeader",

    data (){
        return {
            filmSearch : '',
    
        }
    }

}
</script>

<style lang="scss">

* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}
.myHeadContainer {

    background-color: grey;
    height: 50px;
    padding: 20px;
      
}
    

</style>
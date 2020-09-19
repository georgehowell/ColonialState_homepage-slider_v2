<template>
    <Slider v-if="listing!=''" :listing="listing" />
</template>

<script>
    import Slider from './Slider'
    import json from '../json/forSale.json'
    
  export default {
      name: 'ForSale',
      data(){
          return{
              listing: json,
          }
      },
      components: {
          Slider
      }
  }
</script>
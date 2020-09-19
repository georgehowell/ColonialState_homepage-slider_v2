<template>
    <Slider v-if="listing!=''" :listing="listing" />
</template>

<script>
    import Slider from './Slider'
    import json from '../json/forRent.json'
    
  export default {
      name: 'ForRent',
      data(){
          return{
              listing: json
          }
      },
      components: {
          Slider
      }
  }
</script>
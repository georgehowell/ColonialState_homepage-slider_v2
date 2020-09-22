<template>
    <Slider v-if="listing!=''" :listing="listing"/>
</template>

<script>
    import Slider from './Slider'
    import json from '../json/sold.json'
    
  export default {
      name: 'Sold',
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
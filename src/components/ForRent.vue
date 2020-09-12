<template>
    <slider></slider>
</template>

<script>
    import Slider from './Slider'
    import json from '../json/forRent.json'
    
  export default {
      name: 'ForRent',
      data(){
          return{
              listings: json
          }
      },
      components: {
          'slider': Slider
      }
  }
</script>
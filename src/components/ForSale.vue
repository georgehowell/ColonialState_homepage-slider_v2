<template>
    <slider></slider>
</template>

<script>
    import Slider from './Slider'
    import json from '../json/forSale.json'
    
  export default {
      name: 'ForSale',
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
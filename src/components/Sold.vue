<template>
    <slider></slider>
</template>

<script>
    import Slider from './Slider'
    import json from '../json/sold.json'
    
  export default {
      name: 'Sold',
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
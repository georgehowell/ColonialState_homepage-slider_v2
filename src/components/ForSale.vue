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
                  users: []
          }
      },
      components: {
          Slider
      }
  }
</script>

<style scoped>
</style>
<template>
  <div id="tabs" class="container">
    
      <div class="tabs">
          <a v-on:click="activetab=1" v-bind:class="[ activetab === 1 ? 'active' : '' ]">For Sale</a>
          <a v-on:click="activetab=2" v-bind:class="[ activetab === 2 ? 'active' : '' ]">Sold</a>
          <a v-on:click="activetab=3" v-bind:class="[ activetab === 3 ? 'active' : '' ]">For Rent</a>
      </div>

      <div class="content">
          <div v-if="activetab === 1" class="tabcontent">
              <for-sale></for-sale>
          </div>
          <div v-if="activetab === 2" class="tabcontent">
              <sold></sold>
          </div>
          <div v-if="activetab === 3" class="tabcontent">
              <for-rent></for-rent>
          </div>
      </div>
    
  </div>
</template>

<script>
import ForSale from './components/ForSale.vue'
import Sold from './components/Sold.vue'
import ForRent from './components/ForRent.vue'

export default {
  name: 'App',
  el: '#tabs',
        data() {
            return {
              activetab: 1
            }
        },
  components: {
    'forSale': ForSale,
    'sold': Sold,
    'forRent': ForRent
  }
}
</script>

<style>
/* RESET */
* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

.container {  
    /* max-width: 620px; 
    min-width: 420px; */
    width: 100%;
    margin: 40px auto;
    font-family: Arial, Helvetica, sans-serif;
    font-size: 0.9em;
    color: #888;
}

/* Style the tabs */
.tabs {
    overflow: hidden;
  margin-left: 20px;
    margin-bottom: -2px; 
}

.tabs ul {
    list-style-type: none;
    margin-left: 20px;
}

.tabs a{
    float: left;
    cursor: pointer;
    padding: 12px 24px;
    transition: background-color 0.2s;
    border: 1px solid #ccc;
    border-right: none;
    background-color: #f1f1f1;
    border-radius: 10px 10px 0 0;
    font-weight: bold;
}
.tabs a:last-child { 
    border-right: 1px solid #ccc;
}

/* Change background color of tabs on hover */
.tabs a:hover {
    background-color: #aaa;
    color: #fff;
}

/* Styling for active tab */
.tabs a.active {
    background-color: #fff;
    color: #484848;
    border-bottom: 2px solid #fff;
    cursor: default;
}

/* Style the tab content */
.tabcontent {
    padding: 30px 0;
    border: 1px solid #ccc;
    border-radius: 10px;
  box-shadow: 3px 3px 6px #e1e1e1
}
</style>

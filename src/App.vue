<template>
  <div id="tabs" class="container">
    
      <div class="tabs">
          <a v-on:click="activetab=1" v-bind:class="[ activetab === 1 ? 'active' : '' ]">For Rent</a>
          <a v-on:click="activetab=2" v-bind:class="[ activetab === 2 ? 'active' : '' ]">For Sale</a>
          <a v-on:click="activetab=3" v-bind:class="[ activetab === 3 ? 'active' : '' ]">Sold</a>
      </div>

      <div class="content">
          <div v-if="activetab === 1" class="tabcontent">
              <for-rent></for-rent>
          </div>
          <div v-if="activetab === 2" class="tabcontent">
              <for-sale></for-sale>
          </div>
          <div v-if="activetab === 3" class="tabcontent">
              <sold></sold>
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

<style >
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
    box-shadow: 3px 3px 6px #e1e1e1;
}
#container {
    width: 100%;
    /* display: flex;
    flex-direction: row;
    justify-content: space-between; */
    overflow: hidden ;
    display: block;
}
#container * {
    -webkit-box-sizing:border-box;
	-moz-box-sizing:border-box;
	-o-box-sizing:border-box;
	box-sizing:border-box;
    text-decoration: none !important;
}
.resp-container {
    position: relative;
    overflow: hidden;
    width: 400px;
    height: 300px;
    text-align: left;
}
.resp-container .bg-image {
    width: 100%;
    height: 260px;
    border: 10px #c8c8c8 solid;
    box-shadow: 0 0 10px #888888;
    background-size: cover;
    background-repeat: no-repeat; 
    background-color: #c8c8c8;
    background-position: center center;
}
.resp-container .corner-ribbon {
    float: right;
}
.resp-container h2 {
    font-family: 'Crete Round', serif;
    font-weight: normal;
    line-height: 130%;
    text-align: left;
    height: 100px;
    background-image: linear-gradient(to right, #fff, transparent);
    width: 93.5%;
    margin-top: 0;
    color: #333 !important;
    padding: 0 0 0 12px;
    white-space: initial;
}
.marquee-content-items li a .bg-image h2 {
    color: #333 !important;
    text-decoration: none !important;
}
.resp-container h2 span {
    margin-top: 6px;
    float: right;
    font-family: 'Open Sans', sans-serif;
    font-weight: 800;
    color: #00822c;
    background-color: #fff;
    padding: 0 5px;
    font-size: 16px;
}

.rotate {
    position: absolute;
    right: 3px;
    top: 32px;
    font-size: 22px;
    text-transform: uppercase;
    text-shadow: -1px 1px 1px #000;
    transform: rotate(45deg);
    -webkit-transform: rotate(45deg);
    -moz-transform: rotate(45deg);
    -ms-transform: rotate(45deg);
    -o-transform: rotate(45deg);
    filter: progid:DXImageTransform.Microsoft.BasicImage(rotation=3);
    color: #fff;
    font-family: 'Crete Round', serif;
    font-weight: normal;

}
  

.simple-marquee-container {
    height: 279px;
    background-color: #212059;
    padding: 4px 0 0 0;
}

</style>

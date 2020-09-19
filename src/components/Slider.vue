<template>
    <div id="container">
        <div class="simple-marquee-container">
            <div class="marquee">
                <ul class="marquee-content-items" v-for="(data, key) in listing" :key="key">
                    <li class="resp-container">
                        <img src="../assets/img/corner2.png" class="corner-ribbon" alt="" />
                        <span class="rotate">{{ data.status }}</span>
                        <a :href="data.url" target="_blank">
                            <div class="bg-image" :style="{ backgroundImage: 'url(' + data.heroImg + ')' }">
                                <h2>{{ data.address }}<span>{{ data.price }}</span></h2>
                            </div>
                        </a>
                    </li>
                </ul>
            </div>
        </div>
    </div>
</template>

<script>
    // import json from '../json/forRent.json'
  export default {
      name: 'Slider',
      data(){
          return{
            //   listings: json
          }
      },
    props: {
        listing: Array
    }
  }
</script>

<style scoped>

#container {
    width: 100%;
    /* display: flex;
    flex-direction: row;
    justify-content: space-between; */
    overflow: hidden;
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
    background-size: 100%;
    background-repeat: no-repeat; 
    background-color: #c8c8c8;
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

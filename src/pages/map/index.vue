<template>
  <div class="map">
   <map id="map" longitude="113.324520" latitude="23.099994" scale="14" controls="controls" bindcontroltap="controltap" markers="markers" bindmarkertap="markertap" polyline="polyline" bindregionchange="regionchange" show-location style="width: 100%; height: 600px;"></map>

  </div>
</template>

<script>

export default {

  data () {
    return {
      markers: [{
      iconPath: "/resources/others.png",
      id: 0,
      latitude: 23.099994,
      longitude: 113.324520,
      width: 50,
      height: 50
    }],
    polyline: [{
      points: [{
        longitude: 113.3245211,
        latitude: 23.10229
      }, {
        longitude: 113.324520,
        latitude: 23.21229
      }],
      color:"#FF0000DD",
      width: 2,
      dottedLine: true
    }],
    controls: [{
      id: 1,
      iconPath: '/resources/location.png',
      position: {
        left: 0,
        top: 300 - 50,
        width: 50,
        height: 50
      },
      clickable: true
    }]
    }
  },
  methods:{
      regionchange(e) {
      console.log(e.type)
    },
    markertap(e) {
      console.log(e.markerId)
    },
    controltap(e) {
      console.log(e.controlId)
    }
  }
}
</script>

<style>
.class{
  height:100%;
}

</style>

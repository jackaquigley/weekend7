<template>
  <div id="app">

    <main-data v-if='stats':stats="stats"></main-data>

    </div>

</template
>
<script>

import MainData from './components/MainData.vue'

export default {
  name: 'app',
  props: ['areaData'],
  data() {
    return {
      stats: null
    }
  },
  components: {
    'main-data': MainData
  },
  mounted(){
    fetch('https://api.covid19uk.live')
    .then(res => res.json())
    .then(data => this.stats = data.data[0])
    }
}

</script>

<style>

 #pageTitle {
   text-align: center;
 }

 #main-page {
   border: 1px black solid;
   width: 50%;
 }

</style>

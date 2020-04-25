<template>
  <div id="app">
    <source-topper v-if="stats.length" :stats="stats"></source-topper>
      </div>
</template>
<source-topper>
</source-topper>
<script>

import SourceTopper from './components/SourceTopper.vue'

export default {
  name: 'app',
  data() {
    return {
      stats: [],
      SelectedSource: null
    }
  },
  components: {
    'source-topper': SourceTopper
  },
  mounted(){
    fetch('https://api.covid19uk.live/')
    .then(res => res.json())
    .then(data => this.stats = data.data
    )}
}


</script>

<style>

</style>

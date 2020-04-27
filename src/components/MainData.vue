<template lang="html">
  <div v-if="stats">
  <p>Source: {{stats.source}}</p>

  <p>Confirmed: {{stats.confirmed}}</p>

<p>Deaths: {{stats.death}}</p>

<h4>Tests</h4>

<p>Tests Done: {{stats.test_done}}</p>

<h4>Breakdown By Area</h4>

<p>England: {{stats.england}}</p>

<p>Scotland: {{stats.scotland}}</p>

<p>Nothern Ireland: {{stats.nireland}}</p>

<p>Wales: {{stats.wales}}</p>

<area-data v-for="(areaData, index) in stats.location"
:areaData="areaData"
:key="index"></area-data>

</div>
</template>

<script>

import { eventBus } from '../main.js'
import AreaData from './AreaSearch.vue'

export default {
  name: 'main-data',
  props: ['stats', 'areaData'],
  components: {'area-data': AreaData}
}

</script>

<style lang="css" scoped>
</style>

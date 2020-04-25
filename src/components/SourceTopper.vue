<template lang="html">
  <ul>
    <source-detail v-for="(dataSource, index) in stats"
    :dataSource="dataSource" :key='index'>{{dataSource.name}}</source-detail>
  </ul>
</template>

<script>

import SourceDetail from './SourceDetail.vue'

export default {
  name: 'source-topper',
  props: ['stats'],
  components: {
    "source-detail": SourceDetail
  }
}
</script>

<style lang="css" scoped>
</style>

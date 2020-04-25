<template lang="html">
<div v-if="dataSource">
  <div class="">
  <p>{{dataSource.source}}</p>
</div>
</div>
</template>

<script>
export default {
  name: 'source-detail',
  props: ['dataSource']
}
</script>

<style lang="css" scoped>
</style>

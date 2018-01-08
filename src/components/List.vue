<template lang="html">
  <div>
    <ul v-for="data in list">
      <li>{{data.title}}</li>
    </ul>
  </div>
</template>

<script>
import Store from '../Store'

export default {
  data () {
    return Store
  }
}
</script>

<style lang="css">
</style>

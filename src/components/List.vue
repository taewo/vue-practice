<template lang="html">
  <div class="">
    list
    <ul>
      <li v-for="item in data">
        {{item}}
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  props: [
    'data'
  ],
  created() {
    // console.log('created', this);
  },
  beforeUpdate() {
    console.log('beforeUpdate', this);
  },
  updated() {
    console.log('updated', this);
  }
}
</script>

<style lang="css">
</style>



<!-- <template lang="html">
  <div>
    <h3>This is List component</h3>
    <ul v-for="todo in Store.list">
      <li>
        {{todo.title}}
      </li>
    </ul>
  </div>
</template>

<script>
import Store from '../Store';

export default {
  data () {
    return {
      Store
    }
  }
}
</script>

<style lang="css">
</style>


 -->

<!-- <template lang="html">
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
</style> -->

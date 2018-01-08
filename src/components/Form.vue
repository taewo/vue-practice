<template lang="html">
  <div>
    <h1>{{name.name}} Form</h1>
    <form v-on:submit.prevent>
      <input type="text" v-model="input" />
      <input type="submit" @click="add" />
    </form>
    <h4>{{this.input}}</h4>
  </div>
</template>

<script>
import Store from '../Store'

export default {
  props: ['name', 'city', 'age'],
  methods: {
    hello: function() {
      console.log('hello world');
    },
    check: function(e) {
      console.log('check');
    },
    add () {
      Store.add(this.input)
      this.input = ''
    }
  },
  data () {
    return {
      input: '',
    }
  },
}
</script>

<style lang="css">
</style>

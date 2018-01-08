<template lang="html">
  <div class="">
    Form
    <input
      type="text"
      v-model="myText"
    >
    <input
      type="button"
      value="button"
      @click="selfEvent"
    >
  </div>
</template>

<script>
export default {
  data() {
    return {
      myText: ''
    }
  },

  created() {
    this.myText = this.initText
  },

  methods: {
    selfEvent() {
      this.$emit('myEvent', this.myText)
    }
  },

  props: [
    'initText'
  ]

}
</script>

<style lang="css">
</style>




<!-- <template lang="html">
  <div>
    <h3>This is Form component</h3>
    <form @submit.prevent="submit">
      <input type="text" v-model="input" />
      <input type="submit" value="submit" />
    </form>
  </div>
</template>

<script>
import Store from '../Store'

export default {
  methods: {
    submit: function() {
      console.log(123123123)
      Store.add(this.input)
      this.input = ''
    }
  },
  data () {
    return {
      input: ''
    }
  }
}
</script>

<style lang="css">
</style> -->




<!-- <template lang="html">
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
</style> -->

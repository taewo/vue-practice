<template lang="html">
  <div class="">
    Todo
    <Form
      :handleSubmit="handleSubmit"
      @myEvent="taewoong"
      @myEvent2="taewoong2"
    ></Form>
    <List
      :data="data"
    ></List>
  </div>
</template>

<script>
import Form from './Form'
import List from './List'

export default {
  components: {
    Form,
    List
  },
  data () {
    return {
      input: '',
      data: [],
    }
  },
  methods: {
    handleSubmit: function(param) {
      this.data.push(param)
    },

    taewoong() {
      alert('hi')
    },

    taewoong2(vars) {
      alert(vars)
    }
  }
}
</script>

<style lang="css">
</style>





<!-- <template lang="html">
  <div>
    Todo
    <Form
      @myEvent="onSubmit"
      :initText="abc"/>

    <List
      :data="todos"
    />
  </div>
</template>

<script>
import Form from './Form'
import List from './List'
export default {
  components: {
    Form,
    List
  },
  data () {
    return {
      todos: [],
      abc: '124'
    }
  },
  methods: {
    onSubmit(vars) {
      alert(vars)
      this.todos = this.todos.push(vars)
    }
  }
}
</script>

<style lang="css">
</style> -->



<!-- <template lang="html">
  <div>
    <Form :name="userData"></Form>
    <List nick="asdf"></List>
  </div>
</template>

<script>
import List from './List'
import Form from './Form'

export default {
  components: {
    'Form': Form,
    'List': List,
  },
  data() {
    return {
      name: 'Taewoong',
      age: 11,
      city: 'ANtype',
      userData: {
        name: 'Olim',
        city: 'korea',
      }
    }
  }
}
</script>

<style lang="css">
</style> -->

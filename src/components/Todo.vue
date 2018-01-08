<template lang="html">
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
</style>

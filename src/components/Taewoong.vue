<template lang="html">
  <div class="test">
    <h3>이름: {{name}}</h3>
    <h3>나이: {{age}}</h3>
    <h3>도시: {{city}}</h3>
    <router-link to="/">Go to Foo</router-link>

  </div>
</template>

<script>
export default {
  data() {
    return {
      name: 'Taewoong',
      age: 22,
      city: 'Anyang',
    }
  }
}
</script>

<style lang="css">
</style>

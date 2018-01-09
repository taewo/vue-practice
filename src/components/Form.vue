<template lang="html">
  <div class="">
    <form @submit="submit">
      <input type="text" v-model="userData.name"><br />
      <input type="text" v-model="userData.age"><br />
      <input type="submit" name="" value="제출">
    </form>
  </div>
</template>

<script>
export default {
  data() {
    return {
      userData: {
        name: '',
        age: ''
      }
    }
  },
  methods: {
    submit() {
      console.log('submit');
      this.handleSubmit(this.userData)
      this.userData = {
        name: '',
        age: ''
      }
    }
  },
  props: [
    'handleSubmit'
  ]
}
</script>

<style lang="css">
</style>










<!-- <template lang="html">
  <div class="">
    <form @submit="submit">
      name: <input type="text" v-model="userInfo.name"><br />
      age: <input type="text" v-model="userInfo.age"><br />
      address: <input type="text" v-model="userInfo.address">
      <input type="submit" name="" value="제출">
    </form>
  </div>
</template>

<script>
export default {
  data() {
    return {
      userInfo: {
        name: '',
        age: '',
        address: ''
      }
    }
  },
  props: [
    'handleSubmit'
  ],
  methods: {
    submit() {
      this.handleSubmit(this.userInfo)
      this.userInfo = {
        name: '',
        age: '',
        address: ''
      }
    }
  }
}
</script>

<style lang="css">
</style>
 -->






<!-- <template lang="html">
  <div class="">
    <form @submit.prevent>
      <input type="text" v-model="text">
      <input type="submit" @click="check">

      <input
        type="button"
        value="hi"
        @click="$emit('myEvent')"
      />
      <input type="button" value="hi" @click="mmm" />
      <input type="button" value="ddddd" @click="$emit('myCall')">
    </form>
  </div>
</template>

<script>
export default {
  data () {
    return {
      text: ''
    }
  },
  created() {
    // this.text = this.input
  },
  props: [
    'handleSubmit',
  ],
  methods: {
    check() {
      this.handleSubmit(this.text)
      this.text = ""
    },

    mmm() {
      this.$emit('myEvent2', this.text)
      this.text = ''
    }
  }
}
</script>

<style lang="css">
</style> -->







<!-- <template lang="html">
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
</style> -->




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

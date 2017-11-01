<template>
<div>
  <h1> you did this </h1>

  <div v-once>This will never change: {{ msg }}</div>
  <div>This will be changing: {{ msg | capitalize }}</div>
  <input v-model="msg" placeholder="edit me" v-focus>
  <div>its computed {{ reversedMessage }}</div>
  <p v-if="seen" v-bind:class="{ active: seen }">Now you see me</p>
  <br>
  <a v-on:click.prevent="doSomething">click me</a>
  <p>or</p>
  <a @click="doSomething">me</a>
</div>
</template>

<script>
export default {
  props: {
    propA: Number
  },
  data () {
    return {
      msg: 'my msg',
      seen: false
    }
  },
  computed: {
    reversedMessage: function () {
      return this.msg.split('').reverse().join('')
    }
  },
  methods: {
    doSomething: function () {
      this.msg = 'msg changed'
      this.seen = !this.seen
    }
  },
  filters: {
    capitalize: function (value) {
      if (!value) return ''
      value = value.toString()
      return value.charAt(0).toUpperCase() + value.slice(1)
    }
  },
  directives: {
    focus: {
      inserted: function (el) {
        el.focus()
      }
    }
  }
}
</script>

<style scoped>
a {
  color: #42b983;
  cursor: pointer;
}
.active {
  color: #ff0000;
}
</style>

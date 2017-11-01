<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <h2>Essential Links</h2>
      <a href="https://vuejs.org" target="_blank">Core Docs</a>
      <a href="https://router.vuejs.org/en/essentials/getting-started.html" target="_blank">Vue router</a>
    <h2>Ecosystem</h2>
      <a href="http://router.vuejs.org/" target="_blank">vue-router</a>
      <a href="http://vuex.vuejs.org/" target="_blank">vuex</a>
    <h2> playground</h2>
      <router-link to="/playing-with-vue">Do it yourself</router-link>
  </div>
</template>

<script>
export default {
  name: 'hello',

  data () {
    return {
      msg: 'Welcome guys to our first Vue.js App'
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1, h2 {
  font-weight: normal;
}

ul {
  list-style-type: none;
  padding: 0;
}

li {
  display: inline-block;
  margin: 0 10px;
}

a {
  color: #42b983;
}
</style>

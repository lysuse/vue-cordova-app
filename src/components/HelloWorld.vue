<template>
  <div class="hello">
    <h3>Hello {{appName}}</h3>
    <p>{{msg}}</p>
    <p v-if="!appLoaded">We are Loading ... </p>
    <p v-if="appLoaded">Load Success </p>
  </div>
</template>

<script>
import { mapGetters } from 'vuex'

export default {
  name: 'HelloWorld',
  data () {
    return {
      msg: 'Welcome to Your Vue.js cordova App'
    }
  },
  computed: {
    ...mapGetters(['appName', 'appLoaded'])
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

<template>
  <div class="hello">
  <p>{{msg}}</p>
    <app-message :msg='msg' @messageChanged="msg=$event"></app-message>
  </div>
</template>

<script>
import Message from './Message.vue'
export default {
  name: 'Home',
  data () {
    return {
      msg: 'Home Page'
    }
  },
  components: {
    'app-message': Message
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

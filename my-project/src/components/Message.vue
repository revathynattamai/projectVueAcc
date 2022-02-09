<template>
<div>
<input :value="msg" @input="changeMessage">
<p>{{msg}}</p>
</div>
</template>
<script>
export default {
  props: ['msg'],
  methods: {
    changeMessage (event) {
      this.$emit('messageChanged', event.target.value)
    }
  }
}
</script>

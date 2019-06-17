<template>
  <div class="test">
    this is a test1
  </div>
</template>

<script>
export default {
  name: 'Test',
  props: {
    msg: String
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.test {
    color: red;
}
</style>

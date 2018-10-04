<template>
<div>
  <h1>JcoDo</h1>
  <p>{{ msg }}</p>
</div>
</template>

<script>
export default {
  name: 'JcoDo',
  data () {
    return {
      msg: 'Welcome to your JcoDo List!'
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
ul {
  list-style-type: none;
}
</style>

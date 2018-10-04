<template>
  <div id="app">
    <h1>JcoDo</h1>
    <JcoDo/>
  </div>
</template>

<script>
import JcoDo from './components/JcoDo'

export default {
  name: 'App',
  components: {
    JcoDo
  }
}
</script>

<style>
@import url('https://fonts.googleapis.com/css?family=Lato');
#app {
  font-family: 'Lato', sans-serif;
}
#app h1 {
  margin: 0;
}
</style>

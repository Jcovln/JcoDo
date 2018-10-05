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
body {
  background-color: #DEDEDE;
  color: #282828;
}
input[type="text"] {
  background-color: #C6C6C6;
  border: none;
  padding: 4px;
}
#app {
  font-family: 'Lato', sans-serif;
  font-size: 14pt;
  margin: 30px;
}
#app h1 {
  margin: 0;
  color: #CF2A2A;
}
</style>

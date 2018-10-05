<template>
  <div id="app">
    <div class="container">
      <h1>Jco<span>Do</span></h1>
      <JcoDo/>
    </div>
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
  background-image: linear-gradient(to right, #DC2B2B, #f06d06);
  color: white;
}
.container {
  width: 50%;
  margin: 0 auto;
}
#app {
  font-family: 'Lato', sans-serif;
  font-size: 14pt;
  margin: 30px auto;
}
#app h1 {
  margin: 0;
  color: white;
  text-shadow: 1.5px 1.5px 1.5px #7B0000;
  text-align: center;
}
h1 span {
  color: #FEB923;
}
</style>

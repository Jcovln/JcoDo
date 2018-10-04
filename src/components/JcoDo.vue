<template>
  <div>
    <h2>Inside JcoDo element</h2>
    <ul>
      <li v-for="todo in todos" :key="todo.id">
        {{ todo.text }}
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'JcoDo',
  data () {
    return {
      todos: [
        { text: 'Item 1' },
        { text: 'Item 2' },
        { text: 'Item 3' }
      ]
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

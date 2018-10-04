<template>
  <div class="jcodo-container">
    <ul>
      <li v-for="(todo, index) in todos" :key="todo.id">
        <i class="far fa-times-circle remove" @click="removeTodo(index)"></i> {{ todo.text }}
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
  },
  methods: {
    removeTodo(index) {
      this.todos.splice(index, 1);
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.jcodo-container {
  /* border: 1px solid red; */
}
ul {
  font-size: 12pt;
  list-style-type: none;
  padding: 0 10px;
}
ul li {
  margin: 10px 0;
}
i:hover {
  cursor: pointer;
}
i.remove {
  color: red;
}
</style>

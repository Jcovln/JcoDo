<template>
  <div class="jcodo-container">
    <p>I need to <input type="text" v-model="newTodo" placeholder="do something and press enter" @keyup.enter="addTodo"/></p>
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
      newTodo: '',
      todos: []
    }
  },
  methods: {
    removeTodo (index) {
      this.todos.splice(index, 1)
    },
    addTodo () {
      // Add new todo to the todos array
      this.todos.push({ text: this.newTodo })
      // and clear the input field
      this.newTodo = ''
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
.jcodo-container input {
  width: 200px;
}
</style>

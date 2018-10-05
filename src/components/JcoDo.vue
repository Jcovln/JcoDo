<template>
  <div class="jcodo-container">
    <p>I need to <input type="text" id="in_todo" v-model="newTodo" placeholder="type something and press enter" @keyup.enter="addTodo"/></p>
    <ul>
      <li v-for="(todo, index) in todos" :key="todo.id">
        <i class="fas fa-pencil-alt" @click="editTodo(index)"></i>
        <i class="far fa-times-circle remove" @click="removeTodo(index)"></i>
        {{ todo.text }}
      </li>
    </ul>
  </div>
</template>

<script>

function Capitalize (aString) {
  return aString.charAt(0).toUpperCase() + aString.slice(1)
}

export default {
  name: 'JcoDo',
  data () {
    return {
      newTodo: '',
      todos: []
    }
  },
  mounted () {
    // Focus on the input field
    document.getElementById('in_todo').focus()
    document.getElementById('in_todo').style.width = '270px'
  },
  methods: {
    removeTodo (index) {
      this.todos.splice(index, 1)
    },
    addTodo () {
      // Add new todo to the todos array
      this.todos.push({ text: Capitalize(this.newTodo) })
      // and clear the input field
      this.newTodo = ''
    },
    editTodo (index) {
      // TODO: This should be more robust than a simplistic prompt
      var newDo = prompt('Change this todo: ', this.todos[index].text)
      this.todos[index].text = newDo
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
  color: #CF2A2A;
}
.jcodo-container input {
  background-color: transparent;
  border: none;
  border-bottom: 1px solid gray;
  padding: 4px;
  width: 1px;
  font-size: 14pt;
  outline: none;
  transition: width 1.5s;
}
</style>

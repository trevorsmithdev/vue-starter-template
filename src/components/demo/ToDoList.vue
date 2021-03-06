<template>
  <div>
      <div class="input-wrapper">
          <input v-model="todo" class="todo-input" />
          <button v-on:click="addTodo">Add ToDo</button>
      </div>
      <ul>
          <h2>To Do List</h2>
          <li v-for="(item, index) in todos" v-bind:key="index">{{ item }}</li>
      </ul>
  </div>
</template>

<script>
export default {
    data () {
        return {
            todos: [],
            todo: null
        }
    },
    methods: {
        addTodo () {
            if (this.todo) {
                this.todos.push(this.todo)
                this.todo = null
            }
            
        }
    }

}
</script>

<style>
.todo-input {
    margin-right: 10px;
}
</style>
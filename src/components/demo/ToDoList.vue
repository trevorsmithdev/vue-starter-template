<template>
  <div class="todo-wrapper">
      <div class="input-wrapper">
          <input v-model="todo" class="todo-input" ref="todo" />
          <button class="button" v-on:click="addTodo">Add ToDo</button>
      </div>
      <ul>
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
                this.$refs.todo.focus()
            }
            
        }
    }

}
</script>

<style>
.todo-input {
    font-family: 'Poppins';
    margin-bottom: 10px;
}
.button {
    background-color: #94c9a9;
    font-family: 'Poppins', sans-serif;
    color: #201E1D;
    font-size: 15px;
    cursor: pointer;
    text-decoration: none;
    padding: 0 30px;
    display: block;
    margin: auto;
    font-weight: 600;
    border-radius: 10px;
    border: none;
}
.input-wrapper {
    padding: 10px;
    text-align: center;  
}
.todo-wrapper {
    max-width: 450px;
}
</style>
<template>
  <div>
      <div class="input-wrapper">
          <input v-model="todo" class="todo-input" />
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
            }
            
        }
    }

}
</script>

<style lang="scss">
@import "../../styles/colors.scss";

.todo-input {
    font-family: 'Poppins';
    margin-bottom: 10px;
}
.button {
    background-color: #94c9a9;
    font-family: 'Poppins', sans-serif;
    color: $dark-grey;
    font-size: 15px;
    cursor: pointer;
    text-decoration: none;
    padding: 0 20px;
    display: block;
    margin: auto;
}
.input-wrapper {
    padding: 10px;
    text-align: center;  
}
</style>
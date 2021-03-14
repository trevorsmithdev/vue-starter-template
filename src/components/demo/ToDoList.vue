<template>
  <div class="p-5 max-w-screen-md">
      <div class="text-center">
          <input v-model="todo" class="mb-4 p-1 text-black" ref="todo" />
          <div>
              <button class="btn btn-blue" v-on:click="addTodo">Add ToDo</button>
          </div>
      </div>
      <ul>
          <li v-for="(item, index) in todos" v-bind:key="index">
              <input type="checkbox" class="mr-3" />{{ item }}
          </li>
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

<style lang="postcss">
.btn {
    @apply font-bold py-2 px-4 rounded;
}

.btn-blue {
    @apply bg-blue-500 text-white;
}

.btn-blue:hover {
    @apply bg-blue-700;
}
</style>
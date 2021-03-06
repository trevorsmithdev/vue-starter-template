<template>
  <h1 class="hello-world">{{ message }}</h1>
  <ToDoList />
</template>

<script>
import ToDoList from './components/demo/ToDoList.vue'
export default {
    components: {
      ToDoList
    },
    data () {
        return {
            message: 'Hello World'
        }
    }
}
</script>

<style>
  .hello-world {
      color: red;
  }
</style>
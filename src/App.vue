<template>
  <div class="app-wrapper">
    <h1 class="m-0 text-center">{{ message }}</h1>
    <ToDoList class="border border-dashed m-auto" />
  </div>
  
</template>

<script>
import ToDoList from './components/demo/ToDoList.vue'
export default {
    components: {
      ToDoList
    },
    data () {
        return {
            message: 'Vue Starter Template'
        }
    }
}
</script>

<style lang="postcss">
@import "./styles/variables.scss";

@font-face {
  font-family: 'Poppins';
  src: url('./public/fonts/Poppins-Regular.woff') format('woff');
  font-style: normal;
}
.app-wrapper {
  background-color: $dark-grey;
  color: white;
  min-height: 100vh;
  font-family: 'Poppins';
}
</style>
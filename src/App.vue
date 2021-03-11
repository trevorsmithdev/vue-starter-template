<template>
  <div class="app-wrapper">
    <h1 class="hello-world">{{ message }}</h1>
    <ToDoList class="component" />
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

<style lang="scss">
@import "./styles/colors.scss";

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
  .hello-world {
    text-align: center;
    margin: 0;
  }
  .component {
    border: 1px dashed white;
    margin: 10px
  }
</style>
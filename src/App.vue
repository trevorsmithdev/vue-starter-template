<template>
  <div class="app-wrapper">
    <StickyHeader class="component" />
    <!-- <ToDoList class="border border-dashed m-auto" /> -->
    <BaconIpsum class="p-10" />
  </div>
  
</template>

<script>
import ToDoList from './components/demo/ToDoList.vue'
import StickyHeader from './components/StickyHeader.vue'
import BaconIpsum from './components/BaconIpsum.vue'
export default {
    components: {
      ToDoList,
      StickyHeader,
      BaconIpsum
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
.component {
  @apply border border-dashed;
}
</style>
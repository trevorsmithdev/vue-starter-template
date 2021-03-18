<template>
    <div id="sticky-header" class="flex items-center p-3" :class="[ this.headerIsShrunk ? 'text-xl' : 'text-3xl' ]">
      <h1>Sticky Header</h1>
    </div>
</template>

<script>
export default {
  data() {
    return {
      headerIsShrunk: false
    }
  },
  mounted() {
    window.addEventListener('scroll', this.handleScroll)
  },
  destroyed() {
    window.removeEventListener('scroll', this.handleScroll)
  },
  methods: {
    handleScroll() {
      this.headerIsShrunk = document.body.scrollTop > 50 || document.documentElement.scrollTop > 50
    }
  }
}
</script>

<style lang="postcss">
  #sticky-header {
      height: 11vh;
      background-color: #605856;
      position: fixed;
      top: 0;
      transition: 0.2s;
      width: 100%;
  }
</style>
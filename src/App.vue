<template>
  <div id="app">
    <Menu></Menu>
  </div>
</template>

<script>
import Menu from './components/Menu.vue'

export default {
  name: 'app',
  components: {
    Menu
  }
}
</script>

<style>
#app {
  display: grid;
  grid-template-columns: 30% 70%;
  font-family: sans-serif;
}
</style>

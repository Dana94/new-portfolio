<template>
  <div id="app">
    <Menu></Menu>
    <Projects></Projects>
  </div>
</template>

<script>
import Menu from './components/Menu.vue';
import Projects from './components/Projects.vue'


export default {
  name: 'app',
  components: {
    Menu,
    Projects
  }
}
</script>

<style>
#app {
  display: grid;
  grid-template-columns: 25% 75%;
  font-family: sans-serif;
}
</style>

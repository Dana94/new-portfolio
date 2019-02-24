<template>
  <div id="app">
    <Menu></Menu>
    <component :is="selected"></component>
  </div>
</template>

<script>
import Menu from './components/Menu.vue';
import Projects from './components/Projects.vue';
import About from './components/About.vue';
import Skills from './components/Skills.vue';

import { EventBus } from "./main.js";

export default {
  name: 'app',
  data() {
    return {
      selected: "Projects" //default
    };
  },
  components: {
    Menu,
    Projects,
    About,
    Skills
  },
  mounted() {
    EventBus.$on("new-link", selected => {
      this.selected = selected;
    });
    
  }
}
</script>

<style>
#app {
  display: grid;
  grid-template-columns: 25% 75%;
  font-family: sans-serif;
  /* background-color: #f9f9f9; */
}

html {
  height: 100%;
  background-color: #f9f9f9;
}
</style>

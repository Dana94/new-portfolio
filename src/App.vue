<template>
  <div id="app">
    <Menu></Menu>
    <component :is="selected"></component>
    <i class="fas fa-arrow-circle-up" @click="scrollUp" v-show="scrolled"></i>
  </div>
</template>

<script>
import Menu from "./components/Menu.vue";
import Projects from "./components/Projects.vue";
import About from "./components/About.vue";
import Skills from "./components/Skills.vue";

import { EventBus } from "./main.js";

export default {
  name: "app",
  data() {
    return {
      selected: "Projects", //default
      scrolled: false,
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
    setInterval(()=> {
      // check if user has scolled down the page
      if(window.scrollY > 0) {
        this.scrolled = true;
      } else {
        this.scrolled = false;
      }
    }, 100);
    
  },
  methods: {
    scrollUp: function() {
      window.scroll({
        top: 0,
        left: 0,
        behavior: "smooth"
      });
    }
  }
};
</script>

<style>
#app {
  display: grid;
  grid-template-columns: 1fr;
  font-family: sans-serif;
  /* background-color: #f9f9f9; */
}

html {
  height: 100%;
  background-color: #f9f9f9;
}

.fa-arrow-circle-up {
  position: fixed;
  right: 1rem;
  bottom: 1rem;
  color: rgba(99, 95, 95, 0.89);
  font-size: 3rem;
}

.fa-arrow-circle-up:hover {
  cursor: pointer;
}

@media screen and (min-width: 768px) {
  #app {
    grid-template-columns: 25% 75%;
  }
}
</style>

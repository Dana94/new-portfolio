<template>
  <div class="container">
    <h1>Dana
      <br>Ottaviani
    </h1>
    <h2 @click="select('About')">About</h2>
    <h2 @click="select('Skills')">Skills</h2>
    <h2 @click="select('Projects')">Projects</h2>
    <div class="social">
      <a href="https://github.com/Dana94">
        <i class="fab fa-github fa-2x"></i>
      </a>
      <a href="https://www.linkedin.com/in/danaottaviani/">
        <i class="fab fa-linkedin-in fa-2x"></i>
      </a>
      <a href>
        <i class="fas fa-file fa-2x"></i>
      </a>
      <a href="mailto:dana.ottaviani@gmail.com">
        <i class="fas fa-envelope fa-2x"></i>
      </a>
      <a href>
        <i class="fab fa-free-code-camp fa-2x"></i>
      </a>
    </div>
  </div>
</template>

<script>
import { EventBus } from "../main.js";

export default {
  name: "Menu",
  data() {
    return {
      //selected: "Projects" //default
    };
  },
  methods: {
    select(menuItem) {
      EventBus.$emit("new-link", menuItem);
    }
  }
};
</script>

<style scoped>
.container {
  text-align: center;
  /* position: fixed;
    left: 50px; */
  width: 177px;
}

h2:hover {
  cursor: pointer;
}

.social {
  display: flex;
  flex-direction: column;
  align-items: center;
}

a {
  color: #000000;
  margin: 0 0.5rem;
}

i {
  margin-bottom: 1rem;
}
</style>
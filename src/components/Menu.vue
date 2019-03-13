// use directives for focus
<template>
  <div class="container">
    <div class="fixed">
      <h1>Dana
        <br>Ottaviani
      </h1>
      <div class="menu-links">
        <h2 @click="select('About')">About</h2>
        <h2 @click="select('Skills')">Skills</h2>
        <h2 @click="select('Projects')">Projects</h2>
      </div>
      <div class="social">
        <a href="https://github.com/Dana94" target="_blank">
          <i class="fab fa-github fa-2x"></i>
        </a>
        <a href="https://www.linkedin.com/in/danaottaviani/" target="_blank">
          <i class="fab fa-linkedin-in fa-2x"></i>
        </a>
        <a
          href="https://docs.google.com/document/d/1Oo7dxyvFD4rnVWkhZn1wP6BzO_lNRR_iGHxegOg6Dfw/edit?usp=sharing"
          target="_blank"
        >
          <i class="fas fa-file fa-2x"></i>
        </a>
        <a href="mailto:dana.ottaviani@gmail.com" target="_blank">
          <i class="fas fa-envelope fa-2x"></i>
        </a>
        <a href="https://www.freecodecamp.org/dana94" target="_blank">
          <i class="fab fa-free-code-camp fa-2x"></i>
        </a>
      </div>
    </div>
  </div>
</template>

<script>
import { EventBus } from "../main.js";

export default {
  name: "Menu",
  data() {
    return {};
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
  display: grid;
  grid-template-areas:
    "title"
    "links"
    "social";
    border-bottom: 1px solid;
}

h2:hover {
  cursor: pointer;
}

.social {
  display: flex;
  align-items: center;
  grid-area: social;
  flex-direction: row;
  justify-content: space-around;
  margin: 1rem 0;
}

@media screen and (min-width: 768px) {
  .social,
  .menu-links {
    flex-direction: column;
  }

  .container {
    display: block;
    border-bottom: none;
  }

  .fixed {
    position: fixed;
    width: 25%;
  }
}

.menu-links {
  grid-area: links;
  display: flex;
  justify-content: space-around;
}

a {
  color: #000000;
  margin: 0 0.5rem;
}

i {
  margin-bottom: 1rem;
}

.fa-linkedin-in:hover,
.fa-linkedin-in:focus {
  color: #0077b5;
}

.fa-github:hover {
  color: #28a745;
}

.fa-free-code-camp:hover {
  color: #006400;
}
</style>
<template>
  <ul class="container">
    <li v-for="i in count" :key="i.index"></li>
  </ul>
</template>
<script>
export default {
  data: function() {
    return {
      count: 30
    };
  }
};
</script>
<style scoped>
.container {
  display: grid;
  grid-template-columns: 1fr;
  grid-gap: 1rem;
  margin: 1rem;
  height: 97vh;
  grid-column-start: 1;
  list-style-type: none;
  padding-left: 0;
}

@media screen and (min-width: 768px) {
  .container {
    grid-template-columns: 1fr 1fr 1fr;
    grid-column-start: 2;
  }
}

.container li {
  border: 2px solid;
}

.container li:focus,
.container li:hover {
  border: 2px solid #3fc12e;
  outline: none;
}
</style>


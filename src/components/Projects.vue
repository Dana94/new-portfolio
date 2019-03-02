<template>
  <div class="container">
    <div v-for="i in count" :key="i.index"></div>
  </div>
</template>
<script>
export default {
  data: function() {
    return {
      count: 10
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
}

@media screen and (min-width: 768px) {
  .container {
    grid-template-columns: 1fr 1fr 1fr;
    grid-column-start: 2;
  }
}

.container div {
  border: 1px solid;
}
</style>


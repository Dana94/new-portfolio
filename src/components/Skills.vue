<template>
  <div class="container">
    <h1>Technologies and Frameworks</h1>
    <div class="skills">
      <i class="fab fa-html5 fa-7x"></i>
      <i class="fab fa-css3-alt fa-7x"></i>
      <i class="fab fa-js fa-7x"></i>
      <i class="fab fa-vuejs fa-7x"></i>
      <i class="fab fa-node fa-7x"></i>
      <i class="fab fa-sass fa-7x"></i>
      <img src="../assets/icons/bootstrap-solid.svg" class="bootstrap-icon">
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style scoped>
.skills {
  display: grid;
  grid-template-columns: 1fr 1fr;
  grid-gap: 1rem;
}

@media screen and (min-width: 480px) {
  .skills {
    grid-template-columns: 1fr 1fr 1fr;
  }
}

i,
.bootstrap-icon {
  display: flex;
  justify-content: center;
}

.fa-html5 {
  color: orangered;
}

.fa-js {
  color: #f0db50;
}

.fa-sass {
  color: #cf649a;
}

.fa-node {
  color: #026e00;
}

.fa-css3-alt {
  color: #1673b6;
}

.bootstrap-icon {
  width: 140px;
  height: 112px;
  justify-self: center;
}
</style>


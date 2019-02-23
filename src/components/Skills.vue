<template>
     <div class="container">
         <h1>Skills</h1>
         <div class="skills">
            <i class="fab fa-html5 fa-7x"></i>
            <i class="fab fa-css3-alt fa-7x"></i>
            <i class="fab fa-js fa-7x"></i>
            <i class="fab fa-vuejs fa-7x"></i>
            <i class="fab fa-node fa-7x"></i>
            <i class="fab fa-sass fa-7x"></i>
         </div>
     </div>
</template>

<script>
export default {
    
}
</script>

<style scoped>
.skills {
display: grid;
grid-template-columns: 1fr 1fr 1fr;
grid-gap: 1rem;
}

i {
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
</style>


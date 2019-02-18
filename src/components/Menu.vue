<template>
    <div class="container">
        <h1>Dana <br> Ottaviani</h1>
        <h2>About</h2>
        <h2>Skills</h2>
        <h2>Projects</h2>
        <div class="social">
            <a href="https://github.com/Dana94"><i class="fab fa-github fa-2x"></i></a>
            <a href="https://www.linkedin.com/in/danaottaviani/"><i class="fab fa-linkedin-in fa-2x"></i></a>
            <a href=""><i class="fas fa-file fa-2x"></i></a>
            <a href="mailto:dana.ottaviani@gmail.com"><i class="fas fa-envelope fa-2x"></i></a>
            <a href=""><i class="fab fa-free-code-camp fa-2x"></i></a>
        </div>

    </div>
</template>

<script>
export default {
    name: 'Menu'
}
</script>

<style scoped>
.container {
    text-align: center;
}

.social {
    display: flex;
    justify-content: space-evenly;
}

a {
    color: #000000;
}
</style>
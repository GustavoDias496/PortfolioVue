<script setup>

</script>

<template>
  <div class="container">
    <footer>
        <span class="email">Email: gustavodasilvadias496@gmail.com</span>
        <div class="icons">
          <a href="https://github.com/GustavoDias496" target="_blank"><img src="../assets/github-white.svg" alt=""></a>
          <a href="https://www.linkedin.com/in/gustavodias66/" target="_blank"><img src="../assets/linkedin-white.svg" alt=""></a>
        </div>
    </footer>
  </div>
</template>

<style scoped>
.container{
background-image: linear-gradient(var(--color-gradient-light), var(--color-gradient-dark));
border-top: 3px solid var(--color-margin);
}

footer{
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: space-between;
  padding-left: 30px;
  padding-right: 30px;
}

.sectionPage {
  display: flex;
  align-items: center;
  justify-content: center;
  padding-top: 5em;
}

.email{
  color: var(--color-text-primary);
}

.icons{
  display: flex;
  flex-direction: row;
}

.icons img{
  height: 30px;
  width: 30px;
  padding: 5px;
}

</style>
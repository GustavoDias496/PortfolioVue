<script setup>

</script>

<template>
  <div class="container">
    <section class="sectionPage">
      <div class="imageContainer">
        <img src="../assets/eu2.jpg" alt="">
      </div>
      <div class="aboutContainer">
        <p class="aboutText">
          Olá! Meu nome é Gustavo Dias, atualmente estou cursando o 8º Período de sistemas de informação, meus
          principais
          interesses são em desenvolvimento web e mobile, áreas das quais busco me especializar cada vez mais. Nesse
          portfólio você vai conseguir me conhecer um pouco melhor e ver alguns projetos desenvolvidos.
        </p>
      </div>
    </section>
    <div class="socialContainer">
      <div class="iconContainer">
        <a href="https://github.com/GustavoDias496" target="_blank"><img src="../assets/github-white.svg"
            alt="GitHub"></a>
        <a href="https://github.com/GustavoDias496" target="_blank"><span>GitHub</span></a>
      </div>
      <div class="iconContainer">
        <a href="https://www.linkedin.com/in/gustavodias66/" target="_blank"><img src="../assets/linkedin-white.svg"
            alt="LinkedIn"></a>
        <a href="https://www.linkedin.com/in/gustavodias66/" target="_blank"><span>LinkedIn</span></a>
      </div>
    </div>
  </div>
</template>

<style scoped>
.container {
  height: 92vh;
  background-image: linear-gradient(var(--color-gradient-dark), var(--color-gradient-light));
  padding-top: 8vh;
}

.sectionPage {
  display: flex;
  align-items: center;
  justify-content: center;
  padding-top: 5em;
}

.imageContainer {
  width: 40vw;
  padding: 2em;
}

.imageContainer img {
  width: 250px;
  height: 250px;
  border-radius: 50%;
  border: 3px solid var(--color-margin);
}

.aboutContainer {
  width: 40vw;
}

.aboutContainer p {
  text-align: justify;
  font-weight: 400;
  color: var(--color-text-primary);
}

.socialContainer {
  display: flex;
  align-items: center;
  justify-content: space-evenly;
  padding-top: 2em;
}

.socialContainer img {
  cursor: pointer;
}

.iconContainer {
  display: flex;
  flex-direction: column;
  align-items: center;
}

.iconContainer a {
  text-decoration: none;
}

.iconContainer img {
  height: 50px;
  width: 50px;
}

.iconContainer span {
  font-weight: 500;
  color: var(--color-text-primary);
  margin-top: 7px
}

.iconContainer span:hover {
  cursor: pointer;
}

@media screen and (max-width: 900px) {
  .sectionPage {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
  }

  .imageContainer img {
  width: 150px;
  height: 150px;
  border-radius: 50%;
  border: 3px solid var(--color-margin);
}

.aboutContainer {
  margin: 0 auto;

}

  .imageContainer {
  padding: 0;
  }


.iconContainer img {
  height: 50px;
  width: 50px;
}

}
</style>
<script setup>
import Card from './CardProject.vue'

import projectData from '../data/projectData.json'
const { projects } = projectData;
</script>

<template>
  <div class="container" id="projects">
    <section class="sectionPage">
      <h2 class="title">Projetos</h2>
      <div class="cardsContainer">
        <Card v-for="project in projects" :key="project.id" :name="project.name" :about="project.about"
          :link="project.link" :srcPath="project.srcPath"></Card>
      </div>
    </section>
  </div>
</template>


<style scoped>
.container {
  display: flex;
  align-items: center;
  justify-content: center;
  padding-right: 30px;
  background-image: linear-gradient(var(--color-gradient-light), var(--color-gradient-dark));
}

.sectionPage {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  padding-top: 5em;
}

.title{
  color: var(--color-text-primary);
}

.cardsContainer {
  padding-top: 5em;
  display: grid;
  grid-template-areas: "item item";
  align-items: center;
  column-gap: 20px;
  justify-content: space-evenly;
}

@media screen and (max-width: 900px) {
  .cardsContainer {
  padding-top: 5em;
  display: grid;
  grid-template-areas: 
  "item"
  "item";
  align-items: center;
  row-gap: 5%;
  justify-content: space-evenly;
}
}

</style>
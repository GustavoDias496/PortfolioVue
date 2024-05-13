<script setup>
import CardAbility from './CardAbility.vue'
import languagesData from '../data/abilityData.json'
const { languages } = languagesData;
import frameworksData from '../data/abilityData.json'
const { frameworks } = frameworksData;
import sgbdData from '../data/abilityData.json'
const { sgbd } = sgbdData;
</script>

<template>
  <div class="container" id="skills">
    <section class="sectionPage">
      <h2 class="title">Habilidades</h2>
      <h3 class="subTitle">Linguagens de Programação</h3>
      <div class="cardsContainer">
        <CardAbility v-for="language in languages" 
        :key="language.id" 
        :name="language.name" 
        :srcPath="language.srcPath">
      </CardAbility>
      </div>
      <h3 class="subTitle">Frameworks</h3>
      <div class="cardsContainer">
        <CardAbility v-for="framework in frameworks" 
        :key="framework.id" 
        :name="framework.name" 
        :srcPath="framework.srcPath">
        </CardAbility>
      </div>
      <h3 class="subTitle">SGBD</h3>
      <div class="cardsContainer">
        <CardAbility v-for="sgbd in sgbd" 
        :key="sgbd.id" 
        :name="sgbd.name" 
        :srcPath="sgbd.srcPath">
        </CardAbility>
      </div>
    </section>
  </div>
</template>

<style scoped>
.container {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  padding-right: 30px;
  background-image: linear-gradient(var(--color-gradient-dark), var(--color-gradient-light));
  padding-bottom: 1em;
}

.sectionPage {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  padding-top: 5em;
}

.cardsContainer {
  padding-top: 5em;
  display: grid;
  grid-template-areas: 
  "item item item item";
  align-items: center;
  column-gap: 20px;
  justify-content: space-evenly;
}

.title{
  color: var(--color-text-primary);
}

.subTitle{
  margin-top: 100px;
  color: var(--color-text-primary);
}

@media screen and (max-width: 900px) {
  .cardsContainer {
  padding-top: 5em;
  display: grid;
  grid-template-areas: 
  "item"
  "item"
  "item"
  "item";
  align-items: center;
  row-gap: 5%;
  justify-content: space-evenly;
}
}
</style>
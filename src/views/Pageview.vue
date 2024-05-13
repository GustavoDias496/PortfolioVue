<script setup>
import Inicio from '../components/Inicio.vue'
import Header from '../components/Header.vue'
import Habilidades from '../components/Habilidades.vue'
import Projetos from '../components/Projetos.vue'
import Footer from '../components/Footer.vue'

</script>

<template>
    <main>
        <Header />
        <Inicio />
        <Projetos />
        <Habilidades/>
        <Footer />
    </main>

</template>

<style scoped>
main {
    min-height: 100vh;
    width: 100vw;
}
</style>

<script setup>
import { defineProps } from 'vue'

const props = defineProps(['name', 'srcPath']);

</script>

<template>
    <div class="container" ref="containerRef">
        <span class="name">
            <a :href="link" target="_blank">{{ name }}</a>
        </span>

        <img :src="srcPath" alt="">
        <p class="about">
            {{ about }}
        </p>
    </div>
</template>

<style scoped>
.container {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: space-evenly;
    width: 100px;
    min-height: 100px;
    border-radius: 3px;
    border: 2px solid var(--color-margin);
    padding: 15px;
    background-color: black;
}

.container img {
    width: 50%;
    height: 60%;
    padding-left: 25%;
    padding-right: 25%;
}

.container span {
    margin-bottom: 10px;
}

.container span a {
    text-decoration: none;
    color: var(--color-text-primary);
}

.container p {
    color: var(--color-text-primary);
    font-size: auto;
    margin-top: 10px;
    text-align: justify;
}

.name {
    color: var(--color-margin);
    font-weight: 400;
}
</style>
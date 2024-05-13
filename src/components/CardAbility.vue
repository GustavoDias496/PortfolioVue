<script setup>
import { defineProps } from 'vue'

const props = defineProps(['name', 'srcPath']);

</script>

<template>
    <div class="container" ref="containerRef">
        <span class="name">{{ name }}</span>
        <img :src="srcPath" alt="">
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
}

.container img {
    width: 50%;
    height: auto;
    padding-left: 25%;
    padding-right: 25%;
}

.container span {
    margin-bottom: 10px;
    color: var(--color-margin);
    font-weight: 400;
    text-align: center;
}

.container span a {
    text-decoration: none;
    color: var(--color-text-secondary);
}
</style>
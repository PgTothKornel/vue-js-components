<!-- pascal case -->
<script setup>
import { ref } from 'vue';

const data = [
{ id: 1, name: 'John Doe' },
{ id: 2, name: 'Jane Doe' },

{ id: 3, name: 'Jim Smith' },
{ id: 4, name: 'Sarah Johnson' },
]

const nev = ref('név')
</script>

<template>
    <main>
        <input v-model="nev" type="text" name="nev" id="nev">

        <p v-for="value in data"><span v-show="value.name.includes(nev)">{{ value.name }}</span></p>
    </main>
</template>

<style scoped>
    nav {
        background-color: #f0f0f0;
        padding: 1rem;
    }

    ul {
        display: flex;
        list-style: none;
        padding: 0;
        margin: 0;
    }

    li {
        margin-right: 1rem;
    }

    a {
        text-decoration: none;
        color: #333;
        font-size: 1.2rem;
        padding: 0.5rem 1rem;
    }
</style>

<!-- pascal case -->
<script setup>
const menu = [
{
text: 'Vue.js',
url: 'https://vuejs.org/',
},
{
text: 'React',
url: 'https://reactjs.org/',
},
{
text: 'Angular',
url: 'https://angular.io/',
},
{
text: 'Svelte',
url: 'https://svelte.dev/',
},
]
</script>

<template>
    <nav>
        <p  v-for="value in menu">
        <a :href=value.url>{{ value.text }}</a>
        </p>
    </nav>
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

<script setup>
import {ref} from 'vue';

const props = defineProps(['title'])
console.log(props.title)

const title = ref(props.title)

</script>

<template>
<main>
        <p>Ez itt a teste {{ title }}</p>
    </main>
</template>

<style scoped>
    main {
        background-color: gray;
        border-top: 1px solid #dee2e6;
        padding: 20px 0;
        text-align: center;
    }
</style>

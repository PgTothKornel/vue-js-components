<script setup>
import {ref} from 'vue';
defineProps({
    title: {
        type: String,
        required: true,
        default: 'Test'
    }
})

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

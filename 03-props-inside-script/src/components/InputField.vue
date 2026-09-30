<script setup>
import {ref} from 'vue'

defineEmits(['on-input']);

const name = ref('Név');
</script>

<template>
    <input type="text" placeholder="Enter your name: " @input="$emit('on-input', name)">
</template>

<style scoped>
    
</style>

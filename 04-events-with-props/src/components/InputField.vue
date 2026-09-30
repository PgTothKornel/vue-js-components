<script setup>
import {ref} from 'vue'

defineEmits(['update:modelValue']);
defineProps({
    modelValue: {
        type: String,
        required: true,
        default: ''
    },
    id: {
        type: String,
        required: true
    },
    type: {
        type: String,
        default: 'text',
        required: true
    },
    placeholder: {
        type: String,
        default: '',
        required: true
    },
    label: {
        type: String,
        default: '',
        required: true
    }
})

const name = ref(' ');
</script>

<template>
    <label for="name">{{ label }}: </label>
    <input v-model="name"
    :id="name"
    :type="type" 
    :placeholder="placeholder"
    @input="$emit('update:modelValue', $event.target.value)">
</template>

<style scoped>
    
</style>

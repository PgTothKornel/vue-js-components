<script setup>

import { reactive } from 'vue';
import MainNavigation from './components/MainNavigation.vue';
import DataFilter from './components/DataFilter.vue';

function submitForm() {
  console.log(JSON.stringify(formData));
}

const formData = reactive({
    email: '',
    firstname: '',
    lastname: ''
});




</script>

<template>
  <MainNavigation />
  <br>
  <DataFilter/>

</template>

<style scoped>
</style>

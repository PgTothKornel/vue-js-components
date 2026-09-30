<script setup>
import MainNavigation from './components/MainNavigation.vue';
import SideFooter from './components/SideFooter.vue';
import MainPart from './components/MainPart.vue';
import InputField from './components/InputField.vue';
import {ref } from 'vue';

const title = ref('Vue')

function logMessage(name) {
  console.log("Input changed: " + name)
}

setTimeout(() => {
    title.value = "'react'"
}, 2000);
</script>

<template>
  <header>
    <MainNavigation/>
  </header>

  <main>
    <MainPart  :title="title"/>
    <InputField @on-input="logMessage"/>
  </main>

  <footer>
    <SideFooter/>
  </footer>
</template>

<style scoped>
</style>

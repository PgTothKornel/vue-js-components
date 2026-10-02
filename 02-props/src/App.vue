<script setup>
import MainNavigation from './components/MainNavigation.vue';
import SideFooter from './components/SideFooter.vue';
import SiteContent from './components/SiteContent.vue';
</script>

<template>
  <header>
    <MainNavigation title="Az én Vjú appom!"/>
  </header>

  <main>
    <SiteContent/>
  </main>

  <footer>
    <SideFooter/>
  </footer>
</template>

<style scoped>
</style>

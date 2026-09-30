<script setup>
import MainNavigation from './components/MainNavigation.vue';
import SideFooter from './components/SideFooter.vue';
import MainPart from './components/MainPart.vue';
import InputField from './components/InputField.vue';
import { reactive } from 'vue';

//const title = ref('Vue')
/*
function logMessage(name) {
  console.log("Input changed: " + name)
}
*/
/*setTimeout(() => {
    title.value = "'react'"
}, 2000);*/

function submitForm() {
  console.log(JSON.stringify(formData));
}

const formData = reactive({
    email: '',
    firstname: '',
    lastname: ''
});


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
  <header>
    <MainNavigation/>
  </header>

  <main>
    <MainPart title="Próba"/>
    <InputField v-model="formData.email" id="e-mail" type="email" placeholder="kukac@ku.kac" label="Email adress"/>
    <br>
    <InputField v-model="formData.firstname" id="szin" type="color" placeholder="kék " label="Válassz egy színt: " />
    <br>
    <InputField v-model="formData.lastname" id="age" type="number" placeholder="18" label="Add meg az életkorod" />

    <button @click="submitForm">Submit</button>
  </main>

  <footer>
    <SideFooter/>
  </footer>
</template>

<style scoped>
</style>

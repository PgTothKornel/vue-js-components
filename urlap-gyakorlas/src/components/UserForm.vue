<script setup>
import { ref, computed } from 'vue';

const username = computed(() => {
    
})
const password = computed('')
const confirm = computed('')

const form = ref();

function submitForm() {
    //alert("Név: " + username.value + "  \n" + "Jelszó: " + password.value + "\n" + "Megerősített jelszó: " + confirm.value);
    if (username.value.length > 5 
    && password.value.length > 7 
    && password.value === confirm.value) {
    alert("Név: " + username.value + "  \n" + "Jelszó: " + password.value + "\n" + "Megerősített jelszó: " + confirm.value);
    }
}

</script>

<template>
  <form ref='form' @click.prevent="submitForm">
    <input type="text" name="username" v-model="username" id="username">
    <br>
    <i v-show="username.length < 5">Username must be at least 5 characters long and different from password</i>
    <input type="text" name="password" v-model="password" id="password">
    <br>
    <i v-show="password.length < 8">Password must be at least 8 characters long and different from username</i>
    <input type="text" name="confirm" v-model="confirm" id="confirm">
    <br>
    <i v-show="confirm.length < 8 && confirm.value !== password.value">Confirm password must be at least 8 characters long and match with password</i>

    <button @click="submitForm">Submit</button>
  </form>
</template>

<style scoped>

</style>

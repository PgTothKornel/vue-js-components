<script setup>
import { ref } from 'vue';

const username = ref('');
const password = ref('');
const confirm = ref('');

function submitForm() {
    if (
        username.value.length >= 5 &&
        password.value.length >= 8 &&
        password.value === confirm.value &&
        username.value !== password.value
    ) {
        alert(
            "Név: " + username.value +
            "\nJelszó: " + password.value +
            "\nMegerősített jelszó: " + confirm.value
        );
    }
}
</script>

<template>
  <form @submit.prevent="submitForm">
    <input
      type="text"
      name="username"
      v-model="username"
      id="username"
    >
    <br>

    <i v-show="username.length < 5">
      Username must be at least 5 characters long and different from password
    </i>

    <input
      type="text"
      name="password"
      v-model="password"
      id="password"
    >
    <br>

    <i v-show="password.length < 8">
      Password must be at least 8 characters long and different from username
    </i>

    <input
      type="text"
      name="confirm"
      v-model="confirm"
      id="confirm"
    >
    <br>

    <i v-show="confirm.length < 8 || confirm !== password">
      Confirm password must be at least 8 characters long and match with password
    </i>

    <button type="submit">Submit</button>
  </form>
</template>

<style scoped>
</style>
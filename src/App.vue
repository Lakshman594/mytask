<template>
  <div>
    <h1>Hello, {{ userName }}!</h1>
    <input type="text" v-model="userNameInput" />
    <button @click="updateUserName">Update Name</button>
  </div>
</template>

<script setup>
import { ref } from '@vue/reactivity';

const userName = ref('Vue');
const userNameInput = ref('');

// const formattedUserName = computed(() => {
//   return userName.value.toUpperCase();
// });

function updateUserName() {
  userName.value = userNameInput.value;
}
</script>


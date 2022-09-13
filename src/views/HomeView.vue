<script setup>
import TheWelcome from "@/components/TheWelcome.vue";

let message = $ref("Hello World!");

// setTimeout(() => {
//   message = "I have been changed";
// }, 2000);

let doSomething = () => {
  alert("Doing it now");
};
</script>

<template>
  <main>
    <TheWelcome />
    <p>{{ message }}</p>
    <p>
      <input type="text" v-model="message" />
      <button @click="doSomething">Click Me</button>
    </p>
  </main>
</template>

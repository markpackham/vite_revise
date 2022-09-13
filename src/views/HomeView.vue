<script>
import TheWelcome from "@/components/TheWelcome.vue";
import { ref } from "vue";

export default {
  components: { TheWelcome },

  setup() {
    let message = ref("Hello World!");

    setTimeout(() => {
      message.value = "I have been changed";
    }, 2000);

    return {
      message,
    };
  },

  // data() {
  //   return {
  //     message: "Hello World",
  //   };
  // },

  // mounted() {
  //   alert("I have been mounted");
  // },
};
</script>

<template>
  <main>
    <TheWelcome />
    <p>{{ message }}</p>
    <p>
      <input type="text" v-model="message" />
    </p>
  </main>
</template>

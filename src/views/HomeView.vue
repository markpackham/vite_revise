<!-- <script setup>
import { useFlash } from "@/composables/useFlash";

let { flash } = useFlash();
</script>

<template>
  <main>
    <p>
      <button @click="flash('Test', 'It Works', 'success')">Click Me</button>
    </p>
  </main>
</template> -->

<script setup>
import { ref } from "vue";

let food = ref('');

function write() {
  localStorage.setItem('food', food.value);
}
</script>

<template>
  <div>
    <main>
      <p>
        What is your fav food? <input type="text" v-model="food" @input="write" />
      </p>
    </main>
  </div>
</template>


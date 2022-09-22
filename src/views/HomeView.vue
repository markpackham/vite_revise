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

let food = ref(localStorage.getItem("food"));
let age = ref(localStorage.getItem("age"));

function write(key, value) {
  localStorage.setItem(key, value);

}
</script>

<template>
  <div>
    <main>
      <p>
        What is your fav food? <input type="text" v-model="food" @input="write('food',food)" />
      </p>

      <p>
        How old are you <input type="text" v-model="age" @input="write('age',age)" />
      </p>
    </main>
  </div>
</template>


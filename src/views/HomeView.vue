<script setup>
import { ref, watch } from "vue";
import { useStorage } from "@/composables/useStorage"

let food = useStorage('food');

// let food = ref(localStorage.getItem("food"));
// let age = ref(localStorage.getItem("age"));

// watch(food, (val) => {
//   write('food', val)
// })

// watch(age, (val) => {
//   write('age', val)
// })


// function write(key, value) {
//   localStorage.setItem(key, value);
// }

// setTimeout(() => {
//   food.value = 'changed'
// }, 2000)

</script>

<template>
  <div>
    <main>
      <p>
        What is your fav food? <input type="text" v-model="food" />
      </p>

      <!-- <p>
        How old are you <input type="text" v-model="age" />
      </p> -->
    </main>
  </div>
</template>





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
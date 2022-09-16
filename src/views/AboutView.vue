<script setup>
import { useFlash } from "@/composables/useFlash";

let { flash } = useFlash();
</script>

<template>
  <div>
    <p>
      <button @click="flash('It Works On About')">Click Me</button>
    </p>
  </div>
</template>


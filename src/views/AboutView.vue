<script setup>
import { useFlash } from "@/composables/useFlash";

let { flash } = useFlash();
</script>

<template>
  <div>
    <p>
      <button @click="flash('Info', 'Some info on About', 'info')">
        Click Me
      </button>
    </p>
  </div>
</template>


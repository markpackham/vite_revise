<script>
import { useFlash } from "@/composables/useFlash";

export default {
  setup() {
    let { flash } = useFlash();

    return { flash };
  },
};
</script>

<template>
  <div>
    <p>
      <button @click="flash('It Works On About')">Click Me</button>
    </p>
  </div>
</template>


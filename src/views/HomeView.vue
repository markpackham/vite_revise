<script setup>
import { ref } from "vue";
import TabbableTextarea from "../components/TabbableTextarea.vue";



let comment = ref('Test Value');
</script>

<template>
  <main>
    <div>
      <form>
        <TabbableTextarea v-model="comment" style="width:100%; height:400px;" />
      </form>
    </div>
  </main>
</template>
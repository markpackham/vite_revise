<script setup>

import { ref } from "vue";

let textarea = ref(null);

textarea.addEventListener("keydown", (e) => {
  if (e.keyCode === 9) {
    let val = textarea.value,
      start = textarea.selectionStart,
      end = textarea.selectionEnd;

    textarea.value = val.substring(0, start) + "\t" + val.substring(end);

    textarea.selectionStart = textarea.selectionEnd = start + 1;

    e.preventDefault();
  }
})

</script>

<template>
  <div>
    <form>
      <textarea ref="textarea" style="width: 100%; height:300px">Hello</textarea>
    </form>
  </div>
</template>
<script setup>
import { onMounted, ref } from "vue";

let textarea = ref(null);

function onKeyDown(e) {


  let tarea = textarea.value;

  if (e.keyCode === 9) {
    let val = tarea.value,
      start = tarea.selectionStart,
      end = tarea.selectionEnd;

    tarea.value = val.substring(0, start) + "\t" + val.substring(end);

    tarea.selectionStart = tarea.selectionEnd = start + 1;

    e.preventDefault();
  }

}

</script>

<template>
  <main>
    <div>
      <form>
        <textarea ref="textarea" @keydown="onKeyDown" style="width:100%; height:300px;">Hello</textarea>
      </form>
    </div>
  </main>
</template>
<script setup>
defineProps({
    modelValue: String
})

function onTabPress(e) {

    let tarea = e.target;

    let val = tarea.value,
        start = tarea.selectionStart,
        end = tarea.selectionEnd;

    tarea.value = val.substring(0, start) + "\t" + val.substring(end);

    tarea.selectionStart = tarea.selectionEnd = start + 1;
}
</script>

<template>
    <textarea @keydown.tab.prevent="onTabPress" v-text="modelValue" />
</template>
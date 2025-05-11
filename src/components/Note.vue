<script setup>
import { ref, reactive, useTemplateRef, onMounted, onUpdated, onBeforeMount } from 'vue';

const notes = reactive([]);
const note = ref("");
const noteInput = useTemplateRef("noteInput");
const noteList = useTemplateRef("noteList");

function addNote(){
    notes.push(note.value);
    note.value = "";
    noteInput.value.focus();
    // console.log(noteList.value);
    if (noteList.value) {
        noteList.value.forEach((li) => {
            console.info(li.textContent);
        })
    }
}

onBeforeMount(() => {
    console.info("onBeforeMount");
});

onMounted(() => {
    console.info("onMounted");
    noteInput.value.focus();
});

onUpdated(() => {
    console.info("onUpdated");
});

</script>

<template>
    <h1>Buat Note</h1>
    <div>
        <input ref="noteInput" type="text" v-model="note" placeholder="Tulis note" />
        <button @click="addNote">Tambah Note</button>
    </div>

    <h1>Daftar Note</h1>
    <ul>
        <li v-for="note in notes" ref="noteList">
            {{ note }}
        </li>
    </ul>
</template>

<style scoped>

</style>
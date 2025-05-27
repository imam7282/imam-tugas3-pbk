<template>
  <div>
    <h1>{{ message }}</h1>

    <p :title="tooltip">Arahkan mouse ke teks ini</p>

    <button @click="ubahPesan">Klik untuk ubah pesan</button>

    <input v-model="inputText" placeholder="Tulis sesuatu..." />

    <p v-if="inputText">Kamu menulis: {{ inputText }}</p>
  </div>
</template>

<script setup>
import { ref } from 'vue'

const message = ref('Halo dari Vue!')
const tooltip = 'Ini adalah tooltip'
const inputText = ref('')

function ubahPesan() {
  message.value = 'Pesan telah diubah!'
}
</script>

<style scoped>
h1 {
  color: #42b983;
}
</style>
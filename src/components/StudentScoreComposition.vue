<script setup>
import { ref } from 'vue'

const studentName = ref('')
const score = ref(0)

function addPoints() {
  score.value += 10
}

function deductPoints() {
  score.value -= 5
}

function resetScore() {
  score.value = 0
}
</script>

<template>
  <div>
    <h1>Student Score Manager</h1>

    <label>Student Name:</label>
    <input v-model="studentName" placeholder="Enter Student Name">

    <h2>Student Name: {{ studentName }}</h2>
    <h2>Score: {{ score }}</h2>

    <button @click="addPoints">Add 10 Points</button>
    <button @click="deductPoints">Deduct 5 Points</button>
    <button @click="resetScore">Reset Score</button>
  </div>
</template>
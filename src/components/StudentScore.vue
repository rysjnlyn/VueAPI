<script>
export default {
  data() {
    return {
      studentName: '',
      score: 0
    }
  },

  methods: {
    addPoints() {
      this.score += 10
    },

    deductPoints() {
      this.score -= 5
    },

    resetScore() {
      this.score = 0
    }
  }
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
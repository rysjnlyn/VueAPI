<script>
import { ref } from 'vue'

export default {
  data() {
    return {
      // TASK 1 - Options API
      message: 'Hello World!',

      // TASK 2 - Options API
      studentName: '',
      score: 0
    }
  },

  methods: {
    // TASK 1 - Options API
    changeMessage() {
      this.message = 'Hi World!'
    },

    clear() {
      this.message = ''
    },

    // TASK 2 - Options API
    addPoints() {
      this.score += 10
    },

    deductPoints() {
      this.score -= 5
    },

    resetScore() {
      this.score = 0
    }
  },

  setup() {
    // TASK 1 - Composition API
    const compositionMessage = ref('Hello World!')

    function compositionChangeMessage() {
      compositionMessage.value = 'Hi World!'
    }

    function compositionClear() {
      compositionMessage.value = ''
    }

    // TASK 2 - Composition API
    const compositionStudentName = ref('')
    const compositionScore = ref(0)

    function compositionAddPoints() {
      compositionScore.value += 10
    }

    function compositionDeductPoints() {
      compositionScore.value -= 5
    }

    function compositionResetScore() {
      compositionScore.value = 0
    }

    return {
      compositionMessage,
      compositionChangeMessage,
      compositionClear,

      compositionStudentName,
      compositionScore,
      compositionAddPoints,
      compositionDeductPoints,
      compositionResetScore
    }
  }
}
</script>

<template>
  <div>

    <h2>Options API</h2>

    <h3>{{ message }}</h3>

    <button @click="changeMessage">
      Change Message
    </button>

    <button @click="clear">
      Clear
    </button>

    <hr>

    <h2>Student Score Manager</h2>

    <label>Student Name:</label>
    <input
      v-model="studentName"
      placeholder="Enter Student Name"
    >

    <p>Student Name: {{ studentName }}</p>
    <p>Score: {{ score }}</p>

    <button @click="addPoints">
      Add 10 Points
    </button>

    <button @click="deductPoints">
      Deduct 5 Points
    </button>

    <button @click="resetScore">
      Reset Score
    </button>

  </div>
</template>
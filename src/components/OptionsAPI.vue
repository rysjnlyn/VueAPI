<script>
export default {
  data() {
    return {
      message: 'Hello World!'
    }
  },

  methods: {
    changeMessage() {
      this.message = 'Hi World!'
    },

    clear() {
      this.message = ''
    }
  }
}
</script>

<template>
  <div>
    <h1>{{ message }}</h1>

    <button @click="changeMessage">Change Message</button>
    <button @click="clear">Clear</button>
  </div>
</template>
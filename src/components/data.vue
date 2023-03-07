<template>
  <div>
    <form @submit.prevent="addMessage">
      <input type="text" v-model="message">
      <button type="submit">Добавить</button>
    </form>
    <ul>
      <li v-for="(msg, index) in messages" :key="index">{{ msg }}</li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'UserData',
  data() {
    return {
      message: '',
      messages: []
    }
  },
  methods: {
    addMessage() {
      this.messages.push(this.message)
      this.message = ''
      console.log(this.messages)
    }
  }
}
</script>

<template>
    <div class="login">
      <h2>Login</h2>
      <h3>User: eve.holt@reqres.in Pwd: cityslicka</h3>
      <form @submit.prevent="login">
        <input v-model="email" type="email" placeholder="Email" required>
        <input v-model="password" type="password" placeholder="Password" required>
        <button type="submit">Login</button>
      </form>
      <p v-if="error" class="error">{{ error }}</p>
    </div>
  </template>
  
  <script>
  import axios from 'axios'
  
  export default {
    name: 'LoginForm',
    data() {
      return {
        email: '',
        password: '',
        error: ''
      }
    },
    methods: {
      async login() {
        try {
          const response = await axios.post('https://reqres.in/api/login', {
            email: this.email,
            password: this.password
          })
          if (response.status === 200) {
            this.$emit('login-success')
          }
        } catch (error) {
          this.error = 'Login failed. Please try again.'
        }
      }
    }
  }
  </script>
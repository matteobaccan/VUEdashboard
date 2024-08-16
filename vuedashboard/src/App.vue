<template>
  <div id="app">
    <Login v-if="!isLoggedIn" @login-success="handleLoginSuccess" />
    <Dashboard v-else @logout="handleLogout" />
  </div>
</template>

<script>
import Login from './components/LoginForm.vue'
import Dashboard from './components/DashboardPanel.vue'

export default {
  name: 'App',
  components: {
    Login,
    Dashboard
  },
  data() {
    return {
      isLoggedIn: false
    }
  },
  methods: {
    handleLoginSuccess() {
      this.isLoggedIn = true
    },
    handleLogout() {
      this.isLoggedIn = false
    }
  }
}
</script>
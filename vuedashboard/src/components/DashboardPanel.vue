<template>
    <div class="dashboard">
        <div class="sidebar">
            <h3>Menu</h3>
            <ul>
                <li>Home</li>
                <li>Profile</li>
                <li>Settings</li>
            </ul>
            <button @click="logout">Logout</button>
        </div>
        <div class="main-panel">
            <h2>Welcome to the Dashboard</h2>
            <p>Here you can display your data.</p>
        </div>
    </div>
</template>

<script>
export default {
    name: 'DashboardPanel',
    methods: {
        logout() {
            this.$emit('logout')
        }
    }
}
</script>

<style scoped>
.dashboard {
    display: flex;
}

.sidebar {
    width: 200px;
    padding: 20px;
    background-color: #f0f0f0;
}

.main-panel {
    flex-grow: 1;
    padding: 20px;
}
</style>
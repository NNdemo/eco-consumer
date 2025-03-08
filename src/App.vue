<script setup>
import { computed } from 'vue';
import { useRoute } from 'vue-router';

const route = useRoute();

const showNavbar = computed(() => {
  // Hide navbar on onboarding and quiz pages
  return !['Onboarding', 'Quiz'].includes(route.name);
});
</script>

<template>
  <div class="app-container">
    <div class="app-content">
      <router-view />
    </div>
    <nav v-if="showNavbar" class="bottom-navbar">
      <router-link to="/home" class="nav-item">
        <i class="fas fa-home"></i>
        <span>Home</span>
      </router-link>
      <router-link to="/tracker" class="nav-item">
        <i class="fas fa-leaf"></i>
        <span>Tracker</span>
      </router-link>
      <router-link to="/challenges" class="nav-item">
        <i class="fas fa-trophy"></i>
        <span>Challenges</span>
      </router-link>
      <router-link to="/knowledge" class="nav-item">
        <i class="fas fa-book"></i>
        <span>Learn</span>
      </router-link>
      <router-link to="/profile" class="nav-item">
        <i class="fas fa-user"></i>
        <span>Profile</span>
      </router-link>
    </nav>
  </div>
</template>

<style>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: 'Avenir', 'Helvetica', 'Arial', sans-serif;
}

body {
  background-color: #f5f8f7;
  color: #333;
}

.app-container {
  display: flex;
  flex-direction: column;
  height: 100vh;
  max-width: 500px;
  margin: 0 auto;
  background-color: white;
  position: relative;
}

.app-content {
  flex: 1;
  overflow-y: auto;
  padding-bottom: 70px; /* Space for navbar */
}

.bottom-navbar {
  position: fixed;
  bottom: 0;
  left: 0;
  right: 0;
  max-width: 500px;
  margin: 0 auto;
  display: flex;
  justify-content: space-around;
  background-color: white;
  box-shadow: 0 -2px 10px rgba(0, 0, 0, 0.1);
  height: 60px;
  z-index: 100;
}

.nav-item {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  text-decoration: none;
  color: #869D9A;
  padding: 8px 0;
  width: 20%;
  font-size: 0.8rem;
}

.nav-item i {
  font-size: 1.2rem;
  margin-bottom: 4px;
}

.nav-item.router-link-active {
  color: #2B9B7E;
}

.btn {
  padding: 12px 20px;
  border-radius: 8px;
  border: none;
  font-weight: bold;
  cursor: pointer;
  transition: all 0.3s ease;
}

.btn-primary {
  background-color: #2B9B7E;
  color: white;
}

.btn-secondary {
  background-color: #E8F4F1;
  color: #2B9B7E;
}

.card {
  background: white;
  border-radius: 12px;
  padding: 16px;
  box-shadow: 0 4px 12px rgba(0, 0, 0, 0.05);
  margin-bottom: 16px;
}

h1, h2, h3, h4 {
  color: #2B5E54;
  margin-bottom: 16px;
}
</style>

<template>
  <div class="onboarding">
    <div class="onboarding-content">
      <img class="logo" src="../assets/images/eco_logo.png" alt="EcoConsumer Logo" />
      <h1>Welcome to EcoConsumer</h1>
      <p class="slogan">Live sustainably, make a difference</p>

      <div class="illustration-container">
        <img src="../assets/images/onboarding.jpg" alt="Sustainable Lifestyle" class="illustration" />
      </div>

      <div class="feature-list">
        <div class="feature-item">
          <i class="fas fa-leaf"></i>
          <div class="feature-text">
            <h3>Track your carbon footprint</h3>
            <p>Understand your environmental impact and see how you compare</p>
          </div>
        </div>
        <div class="feature-item">
          <i class="fas fa-lightbulb"></i>
          <div class="feature-text">
            <h3>Get personalized tips</h3>
            <p>Receive customized suggestions to live more sustainably</p>
          </div>
        </div>
        <div class="feature-item">
          <i class="fas fa-trophy"></i>
          <div class="feature-text">
            <h3>Complete challenges</h3>
            <p>Join fun challenges and earn badges for sustainable actions</p>
          </div>
        </div>
      </div>

      <router-link to="/quiz" class="btn btn-primary get-started">
        Take the Quiz to Get Started
      </router-link>
    </div>
  </div>
</template>

<script setup>
// No data needed for this component
</script>

<style scoped>
.onboarding {
  min-height: 100vh;
  padding: 2rem;
  display: flex;
  flex-direction: column;
  align-items: center;
  text-align: center;
}

.logo {
  width: 80px;
  height: 80px;
  object-fit: cover;
  border-radius: 50%;
  margin-bottom: 1rem;
}

h1 {
  color: #2B5E54;
  font-size: 2rem;
  margin-bottom: 0.5rem;
}

.slogan {
  color: #6A8D87;
  font-size: 1.1rem;
  margin-bottom: 2rem;
}

.illustration-container {
  width: 100%;
  margin-bottom: 2rem;
}

.illustration {
  width: 100%;
  max-width: 300px;
  height: auto;
  border-radius: 12px;
}

.feature-list {
  margin-bottom: 2rem;
  width: 100%;
}

.feature-item {
  display: flex;
  align-items: flex-start;
  text-align: left;
  margin-bottom: 1.5rem;
}

.feature-item i {
  font-size: 1.5rem;
  color: #2B9B7E;
  margin-right: 1rem;
  margin-top: 0.2rem;
}

.feature-text h3 {
  font-size: 1.1rem;
  margin-bottom: 0.5rem;
  color: #2B5E54;
}

.feature-text p {
  font-size: 0.9rem;
  color: #6A8D87;
}

.get-started {
  display: block;
  width: 100%;
  padding: 1rem;
  font-size: 1.1rem;
  text-align: center;
  text-decoration: none;
}
</style> 
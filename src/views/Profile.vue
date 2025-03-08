<template>
  <div class="profile-container">
    <header class="profile-header">
      <div class="profile-image-container">
        <div class="profile-image">
          <i class="fas fa-user"></i>
        </div>
        <button class="edit-profile-btn">
          <i class="fas fa-pencil-alt"></i>
        </button>
      </div>
      <h1>Sarah Johnson</h1>
      <p class="profile-tag">Eco Enthusiast</p>
    </header>

    <!-- Stats Overview -->
    <section class="stats-overview">
      <div class="stat-card">
        <span class="stat-value">340</span>
        <span class="stat-label">Eco Points</span>
      </div>
      <div class="stat-card">
        <span class="stat-value">7</span>
        <span class="stat-label">Badges</span>
      </div>
      <div class="stat-card">
        <span class="stat-value">12</span>
        <span class="stat-label">Challenges</span>
      </div>
    </section>

    <!-- Carbon Overview -->
    <section class="carbon-overview card">
      <div class="section-header">
        <h2>Carbon Footprint</h2>
        <router-link to="/tracker" class="view-details">Details</router-link>
      </div>
      <div class="carbon-summary">
        <div class="carbon-chart-mini">
          <div class="chart-circle">
            <div class="inner-circle">
              <span>3.4</span>
              <span class="unit">tons</span>
            </div>
          </div>
        </div>
        <div class="carbon-text">
          <p>Your carbon footprint is <strong>24% lower</strong> than the average user.</p>
          <p>You've reduced your footprint by <strong>12%</strong> since you started.</p>
        </div>
      </div>
    </section>

    <!-- Badges -->
    <section class="badges-section card">
      <div class="section-header">
        <h2>Your Badges</h2>
        <span class="view-all">View All</span>
      </div>
      <div class="badges-grid">
        <div class="badge-item">
          <div class="badge-icon">
            <i class="fas fa-recycle"></i>
          </div>
          <span class="badge-name">Recycling Pro</span>
        </div>
        <div class="badge-item">
          <div class="badge-icon">
            <i class="fas fa-leaf"></i>
          </div>
          <span class="badge-name">Green Thumb</span>
        </div>
        <div class="badge-item">
          <div class="badge-icon">
            <i class="fas fa-walking"></i>
          </div>
          <span class="badge-name">Green Commuter</span>
        </div>
        <div class="badge-item">
          <div class="badge-icon">
            <i class="fas fa-lightbulb"></i>
          </div>
          <span class="badge-name">Energy Saver</span>
        </div>
        <div class="badge-item">
          <div class="badge-icon inactive">
            <i class="fas fa-shopping-bag"></i>
          </div>
          <span class="badge-name">Smart Shopper</span>
        </div>
        <div class="badge-item">
          <div class="badge-icon inactive">
            <i class="fas fa-utensils"></i>
          </div>
          <span class="badge-name">Sustainable Eater</span>
        </div>
      </div>
    </section>

    <!-- Settings -->
    <section class="settings-section">
      <h2>Settings</h2>
      <div class="settings-menu">
        <div class="menu-item">
          <div class="menu-icon">
            <i class="fas fa-user-cog"></i>
          </div>
          <div class="menu-text">
            <h3>Account Settings</h3>
            <p>Update your profile and preferences</p>
          </div>
          <i class="fas fa-chevron-right"></i>
        </div>
        <div class="menu-item">
          <div class="menu-icon">
            <i class="fas fa-bell"></i>
          </div>
          <div class="menu-text">
            <h3>Notifications</h3>
            <p>Manage your notification settings</p>
          </div>
          <i class="fas fa-chevron-right"></i>
        </div>
        <div class="menu-item">
          <div class="menu-icon">
            <i class="fas fa-shield-alt"></i>
          </div>
          <div class="menu-text">
            <h3>Privacy</h3>
            <p>Control your data and privacy settings</p>
          </div>
          <i class="fas fa-chevron-right"></i>
        </div>
        <div class="menu-item">
          <div class="menu-icon">
            <i class="fas fa-question-circle"></i>
          </div>
          <div class="menu-text">
            <h3>Help & Support</h3>
            <p>Get assistance and contact support</p>
          </div>
          <i class="fas fa-chevron-right"></i>
        </div>
        <div class="menu-item">
          <div class="menu-icon">
            <i class="fas fa-comment-alt"></i>
          </div>
          <div class="menu-text">
            <h3>Feedback</h3>
            <p>Share your thoughts and suggestions</p>
          </div>
          <i class="fas fa-chevron-right"></i>
        </div>
      </div>

      <button class="btn btn-secondary logout-btn">
        <i class="fas fa-sign-out-alt"></i> Log Out
      </button>
    </section>
  </div>
</template>

<script setup>
// Static data for demo
</script>

<style scoped>
.profile-container {
  padding: 1.5rem;
  padding-bottom: 5rem;
}

.profile-header {
  display: flex;
  flex-direction: column;
  align-items: center;
  margin-bottom: 2rem;
}

.profile-image-container {
  position: relative;
  margin-bottom: 1rem;
}

.profile-image {
  width: 100px;
  height: 100px;
  border-radius: 50%;
  background-color: #E8F4F1;
  display: flex;
  align-items: center;
  justify-content: center;
}

.profile-image i {
  font-size: 2.5rem;
  color: #2B9B7E;
}

.edit-profile-btn {
  position: absolute;
  bottom: 0;
  right: 0;
  width: 32px;
  height: 32px;
  background-color: #2B9B7E;
  border: none;
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
  color: white;
  cursor: pointer;
}

h1 {
  font-size: 1.5rem;
  margin-bottom: 0.5rem;
}

.profile-tag {
  color: #6A8D87;
  background-color: #E8F4F1;
  padding: 0.3rem 1rem;
  border-radius: 20px;
  font-size: 0.9rem;
}

.stats-overview {
  display: flex;
  justify-content: space-between;
  margin-bottom: 2rem;
}

.stat-card {
  flex: 1;
  background-color: white;
  border-radius: 10px;
  padding: 1rem;
  text-align: center;
  box-shadow: 0px 4px 12px rgba(0, 0, 0, 0.05);
  margin: 0 0.5rem;
}

.stat-card:first-child {
  margin-left: 0;
}

.stat-card:last-child {
  margin-right: 0;
}

.stat-value {
  display: block;
  font-size: 1.5rem;
  font-weight: bold;
  color: #2B9B7E;
  margin-bottom: 0.5rem;
}

.stat-label {
  font-size: 0.85rem;
  color: #6A8D87;
}

.section-header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-bottom: 1rem;
}

h2 {
  font-size: 1.2rem;
  margin-bottom: 0;
}

.view-details, .view-all {
  color: #2B9B7E;
  font-size: 0.9rem;
  font-weight: 600;
  text-decoration: none;
  cursor: pointer;
}

.carbon-overview, .badges-section {
  margin-bottom: 2rem;
  padding: 1.5rem;
}

.carbon-summary {
  display: flex;
  align-items: center;
}

.carbon-chart-mini {
  margin-right: 1.5rem;
}

.chart-circle {
  width: 80px;
  height: 80px;
  border-radius: 50%;
  background: conic-gradient(#2B9B7E 0% 70%, #E8F4F1 70% 100%);
  display: flex;
  align-items: center;
  justify-content: center;
  position: relative;
}

.inner-circle {
  width: 60px;
  height: 60px;
  border-radius: 50%;
  background-color: white;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  font-weight: bold;
  color: #2B9B7E;
}

.unit {
  font-size: 0.7rem;
  font-weight: normal;
  color: #6A8D87;
}

.carbon-text p {
  margin-bottom: 0.5rem;
  font-size: 0.95rem;
  color: #4A4A4A;
}

.badges-grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 1rem;
}

.badge-item {
  display: flex;
  flex-direction: column;
  align-items: center;
  text-align: center;
}

.badge-icon {
  width: 50px;
  height: 50px;
  border-radius: 50%;
  background-color: #E8F4F1;
  display: flex;
  align-items: center;
  justify-content: center;
  margin-bottom: 0.5rem;
}

.badge-icon i {
  font-size: 1.2rem;
  color: #2B9B7E;
}

.badge-icon.inactive {
  background-color: #F5F5F5;
}

.badge-icon.inactive i {
  color: #BBBBBB;
}

.badge-name {
  font-size: 0.8rem;
}

.settings-section {
  margin-bottom: 2rem;
}

.settings-menu {
  margin-bottom: 2rem;
}

.menu-item {
  display: flex;
  align-items: center;
  background-color: white;
  padding: 1rem;
  border-radius: 10px;
  margin-bottom: 0.5rem;
  box-shadow: 0px 2px 6px rgba(0, 0, 0, 0.05);
}

.menu-icon {
  width: 40px;
  height: 40px;
  border-radius: 10px;
  background-color: #E8F4F1;
  display: flex;
  align-items: center;
  justify-content: center;
  margin-right: 1rem;
}

.menu-icon i {
  color: #2B9B7E;
}

.menu-text {
  flex: 1;
}

.menu-text h3 {
  font-size: 1rem;
  margin-bottom: 0.2rem;
}

.menu-text p {
  font-size: 0.85rem;
  color: #6A8D87;
  margin-bottom: 0;
}

.menu-item i.fa-chevron-right {
  color: #6A8D87;
}

.logout-btn {
  width: 100%;
  display: flex;
  justify-content: center;
  align-items: center;
  padding: 1rem;
}

.logout-btn i {
  margin-right: 0.5rem;
}
</style> 
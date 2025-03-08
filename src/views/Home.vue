<template>
  <div class="home-container">
    <!-- Header -->
    <header class="home-header">
      <div class="welcome-section">
        <h1>Hello, Sarah!</h1>
        <div class="eco-points">
          <span class="points">340</span>
          <span class="label">Eco Points</span>
        </div>
      </div>
    </header>

    <!-- Quick Actions -->
    <section class="quick-actions">
      <div class="action-button record-button">
        <i class="fas fa-plus"></i>
        <span>Record Activity</span>
      </div>
      <div class="action-button challenge-button">
        <i class="fas fa-trophy"></i>
        <span>Daily Challenge</span>
      </div>
    </section>

    <!-- Today's Tip -->
    <section class="card today-tip">
      <div class="tip-header">
        <h3>Today's Eco Tip</h3>
        <i class="fas fa-lightbulb tip-icon"></i>
      </div>
      <p class="tip-content">Take reusable bags when shopping today - a single plastic bag takes up to 1,000 years to decompose!</p>
      <div class="tip-actions">
        <button class="btn-text">Share</button>
        <button class="btn-text">More Tips</button>
      </div>
    </section>

    <!-- Achievements -->
    <section class="achievements-section">
      <div class="section-header">
        <h3>Your Achievements</h3>
        <router-link to="/profile" class="view-all">View All</router-link>
      </div>
      <div class="badges-container">
        <div class="badge">
          <div class="badge-icon">
            <i class="fas fa-recycle"></i>
          </div>
          <span>Recycling Pro</span>
        </div>
        <div class="badge">
          <div class="badge-icon">
            <i class="fas fa-walking"></i>
          </div>
          <span>Green Commuter</span>
        </div>
        <div class="badge">
          <div class="badge-icon inactive">
            <i class="fas fa-shopping-bag"></i>
          </div>
          <span>Smart Shopper</span>
        </div>
      </div>
    </section>

    <!-- Sustainable Products -->
    <section class="products-section">
      <div class="section-header">
        <h3>Eco-Friendly Products</h3>
        <span class="view-all">View All</span>
      </div>
      <div class="products-carousel">
        <div class="product-card">
          <img src="../assets/images/eco_product1.jpg" alt="Reusable Water Bottle" class="product-image">
          <div class="product-info">
            <h4>Bamboo Toothbrush</h4>
            <p>Sustainable alternative to plastic</p>
            <div class="product-rating">
              <i class="fas fa-star"></i>
              <i class="fas fa-star"></i>
              <i class="fas fa-star"></i>
              <i class="fas fa-star"></i>
              <i class="fas fa-star-half-alt"></i>
              <span>4.5</span>
            </div>
          </div>
        </div>
        <div class="product-card">
          <img src="../assets/images/eco_product2.jpg" alt="Reusable Shopping Bags" class="product-image">
          <div class="product-info">
            <h4>Cotton Produce Bags</h4>
            <p>Set of 5 reusable bags</p>
            <div class="product-rating">
              <i class="fas fa-star"></i>
              <i class="fas fa-star"></i>
              <i class="fas fa-star"></i>
              <i class="fas fa-star"></i>
              <i class="far fa-star"></i>
              <span>4.0</span>
            </div>
          </div>
        </div>
        <div class="product-card">
          <img src="../assets/images/eco_product3.jpg" alt="Bamboo Cutlery Set" class="product-image">
          <div class="product-info">
            <h4>Bamboo Cutlery Set</h4>
            <p>Portable and eco-friendly</p>
            <div class="product-rating">
              <i class="fas fa-star"></i>
              <i class="fas fa-star"></i>
              <i class="fas fa-star"></i>
              <i class="fas fa-star"></i>
              <i class="fas fa-star"></i>
              <span>5.0</span>
            </div>
          </div>
        </div>
      </div>
    </section>
  </div>
</template>

<script setup>
// Static data for demo
</script>

<style scoped>
.home-container {
  padding: 1.5rem;
  padding-bottom: 5rem;
}

.home-header {
  margin-bottom: 1.5rem;
}

.welcome-section {
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.welcome-section h1 {
  font-size: 1.5rem;
  margin-bottom: 0;
}

.eco-points {
  display: flex;
  flex-direction: column;
  align-items: flex-end;
}

.points {
  color: #2B9B7E;
  font-size: 1.2rem;
  font-weight: bold;
}

.label {
  font-size: 0.8rem;
  color: #6A8D87;
}

.quick-actions {
  display: flex;
  gap: 1rem;
  margin-bottom: 1.5rem;
}

.action-button {
  flex: 1;
  background-color: #E8F4F1;
  border-radius: 10px;
  padding: 1rem;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  cursor: pointer;
  transition: all 0.2s ease;
}

.action-button:hover {
  background-color: #2B9B7E;
  color: white;
}

.action-button i {
  font-size: 1.5rem;
  margin-bottom: 0.5rem;
  color: #2B9B7E;
}

.action-button:hover i {
  color: white;
}

.today-tip {
  margin-bottom: 1.5rem;
}

.tip-header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-bottom: 1rem;
}

.tip-header h3 {
  margin-bottom: 0;
}

.tip-icon {
  color: #F9A826;
  font-size: 1.5rem;
}

.tip-content {
  font-size: 0.95rem;
  line-height: 1.5;
  margin-bottom: 1rem;
}

.tip-actions {
  display: flex;
  justify-content: flex-end;
  gap: 1rem;
}

.btn-text {
  background: none;
  border: none;
  color: #2B9B7E;
  font-weight: 600;
  cursor: pointer;
}

.section-header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-bottom: 1rem;
}

.section-header h3 {
  margin-bottom: 0;
  font-size: 1.2rem;
}

.view-all {
  color: #2B9B7E;
  font-size: 0.9rem;
  font-weight: 600;
  cursor: pointer;
  text-decoration: none;
}

.badges-container {
  display: flex;
  gap: 1rem;
  margin-bottom: 1.5rem;
  overflow-x: auto;
  padding-bottom: 0.5rem;
}

.badge {
  display: flex;
  flex-direction: column;
  align-items: center;
  min-width: 80px;
}

.badge-icon {
  width: 60px;
  height: 60px;
  border-radius: 50%;
  background-color: #E8F4F1;
  display: flex;
  align-items: center;
  justify-content: center;
  margin-bottom: 0.5rem;
}

.badge-icon i {
  font-size: 1.5rem;
  color: #2B9B7E;
}

.badge-icon.inactive {
  background-color: #F5F5F5;
}

.badge-icon.inactive i {
  color: #BBBBBB;
}

.badge span {
  font-size: 0.8rem;
  text-align: center;
}

.products-carousel {
  display: flex;
  gap: 1rem;
  overflow-x: auto;
  padding-bottom: 1rem;
}

.product-card {
  min-width: 200px;
  background-color: white;
  border-radius: 10px;
  overflow: hidden;
  box-shadow: 0px 4px 12px rgba(0, 0, 0, 0.05);
}

.product-image {
  width: 100%;
  height: 150px;
  object-fit: cover;
}

.product-info {
  padding: 1rem;
}

.product-info h4 {
  margin-bottom: 0.5rem;
  font-size: 1rem;
}

.product-info p {
  color: #6A8D87;
  font-size: 0.85rem;
  margin-bottom: 0.5rem;
}

.product-rating {
  display: flex;
  align-items: center;
}

.product-rating i {
  color: #F9A826;
  font-size: 0.9rem;
}

.product-rating span {
  margin-left: 0.5rem;
  font-weight: 600;
  font-size: 0.9rem;
}
</style> 
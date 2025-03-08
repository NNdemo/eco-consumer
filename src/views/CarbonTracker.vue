<template>
  <div class="tracker-container">
    <header class="tracker-header">
      <h1>Carbon Footprint</h1>
      <div class="period-selector">
        <button class="period-btn active">Month</button>
        <button class="period-btn">Year</button>
      </div>
    </header>

    <!-- Carbon Summary -->
    <section class="carbon-summary card">
      <div class="summary-content">
        <div class="carbon-score">
          <div class="score-circle">
            <span class="score">3.4</span>
            <span class="unit">tons</span>
          </div>
          <div class="score-label">Carbon Footprint</div>
        </div>
        <div class="carbon-comparison">
          <div class="comparison-item">
            <span class="comparison-label">vs. Last Month</span>
            <span class="comparison-value decrease">-12%</span>
          </div>
          <div class="comparison-item">
            <span class="comparison-label">vs. Average</span>
            <span class="comparison-value decrease">-24%</span>
          </div>
        </div>
      </div>
      <div class="carbon-chart">
        <!-- Chart would be implemented with chart.js -->
        <div class="chart-placeholder">
          <div class="bar" style="height: 50px;"></div>
          <div class="bar" style="height: 70px;"></div>
          <div class="bar" style="height: 60px;"></div>
          <div class="bar" style="height: 45px;"></div>
          <div class="bar active" style="height: 35px;"></div>
        </div>
      </div>
    </section>

    <!-- Category Breakdown -->
    <section class="category-breakdown">
      <h2>Breakdown by Category</h2>
      <div class="categories">
        <div class="category-card">
          <div class="category-icon transport">
            <i class="fas fa-car"></i>
          </div>
          <div class="category-info">
            <div class="category-header">
              <h3>Transport</h3>
              <span class="category-value">1.2 tons</span>
            </div>
            <div class="category-progress">
              <div class="progress-bar" style="width: 35%;"></div>
            </div>
          </div>
        </div>
        <div class="category-card">
          <div class="category-icon home">
            <i class="fas fa-home"></i>
          </div>
          <div class="category-info">
            <div class="category-header">
              <h3>Home Energy</h3>
              <span class="category-value">0.9 tons</span>
            </div>
            <div class="category-progress">
              <div class="progress-bar" style="width: 27%;"></div>
            </div>
          </div>
        </div>
        <div class="category-card">
          <div class="category-icon food">
            <i class="fas fa-utensils"></i>
          </div>
          <div class="category-info">
            <div class="category-header">
              <h3>Food</h3>
              <span class="category-value">0.8 tons</span>
            </div>
            <div class="category-progress">
              <div class="progress-bar" style="width: 24%;"></div>
            </div>
          </div>
        </div>
        <div class="category-card">
          <div class="category-icon shopping">
            <i class="fas fa-shopping-bag"></i>
          </div>
          <div class="category-info">
            <div class="category-header">
              <h3>Shopping</h3>
              <span class="category-value">0.5 tons</span>
            </div>
            <div class="category-progress">
              <div class="progress-bar" style="width: 14%;"></div>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- Recent Activities -->
    <section class="recent-activities">
      <div class="section-header">
        <h2>Recent Activities</h2>
        <button class="btn btn-primary add-activity">
          <i class="fas fa-plus"></i> Add
        </button>
      </div>
      <div class="activities-list">
        <div class="activity-item">
          <div class="activity-icon transport">
            <i class="fas fa-car"></i>
          </div>
          <div class="activity-details">
            <div class="activity-main">
              <h4>Car Travel</h4>
              <span class="activity-impact">+2.4 kg CO₂</span>
            </div>
            <div class="activity-meta">
              <span class="activity-date">Today, 2:30 PM</span>
              <span class="activity-description">15 km trip to work</span>
            </div>
          </div>
        </div>
        <div class="activity-item">
          <div class="activity-icon food">
            <i class="fas fa-utensils"></i>
          </div>
          <div class="activity-details">
            <div class="activity-main">
              <h4>Vegetarian Meal</h4>
              <span class="activity-impact positive">-1.2 kg CO₂</span>
            </div>
            <div class="activity-meta">
              <span class="activity-date">Yesterday, 7:15 PM</span>
              <span class="activity-description">Instead of beef burger</span>
            </div>
          </div>
        </div>
        <div class="activity-item">
          <div class="activity-icon home">
            <i class="fas fa-lightbulb"></i>
          </div>
          <div class="activity-details">
            <div class="activity-main">
              <h4>LED Bulb Installation</h4>
              <span class="activity-impact positive">-0.8 kg CO₂</span>
            </div>
            <div class="activity-meta">
              <span class="activity-date">Feb 28, 10:00 AM</span>
              <span class="activity-description">Replaced 5 bulbs</span>
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
.tracker-container {
  padding: 1.5rem;
  padding-bottom: 5rem;
}

.tracker-header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-bottom: 1.5rem;
}

h1 {
  font-size: 1.5rem;
  margin-bottom: 0;
}

.period-selector {
  display: flex;
  background-color: #F5F8F7;
  border-radius: 20px;
  overflow: hidden;
}

.period-btn {
  padding: 0.5rem 1rem;
  border: none;
  background: none;
  cursor: pointer;
  font-weight: 600;
  color: #6A8D87;
}

.period-btn.active {
  background-color: #2B9B7E;
  color: white;
}

.carbon-summary {
  margin-bottom: 2rem;
  padding: 1.5rem;
}

.summary-content {
  display: flex;
  justify-content: space-between;
  margin-bottom: 1.5rem;
}

.carbon-score {
  display: flex;
  flex-direction: column;
  align-items: center;
}

.score-circle {
  width: 80px;
  height: 80px;
  border-radius: 50%;
  background-color: #E8F4F1;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  margin-bottom: 0.5rem;
}

.score {
  font-size: 1.8rem;
  font-weight: bold;
  color: #2B9B7E;
  line-height: 1;
}

.unit {
  font-size: 0.8rem;
  color: #6A8D87;
}

.score-label {
  font-size: 0.9rem;
  color: #6A8D87;
}

.carbon-comparison {
  display: flex;
  flex-direction: column;
  justify-content: center;
}

.comparison-item {
  margin-bottom: 1rem;
  display: flex;
  flex-direction: column;
}

.comparison-label {
  font-size: 0.9rem;
  color: #6A8D87;
  margin-bottom: 0.2rem;
}

.comparison-value {
  font-weight: bold;
  font-size: 1.1rem;
}

.decrease {
  color: #2B9B7E;
}

.increase {
  color: #E74C3C;
}

.carbon-chart {
  height: 100px;
}

.chart-placeholder {
  height: 100%;
  display: flex;
  justify-content: space-between;
  align-items: flex-end;
}

.bar {
  width: 18%;
  background-color: #E8F4F1;
  border-radius: 4px 4px 0 0;
}

.bar.active {
  background-color: #2B9B7E;
}

.category-breakdown {
  margin-bottom: 2rem;
}

h2 {
  font-size: 1.2rem;
  margin-bottom: 1rem;
}

.categories {
  display: flex;
  flex-direction: column;
  gap: 1rem;
}

.category-card {
  display: flex;
  background-color: white;
  border-radius: 10px;
  padding: 1rem;
  box-shadow: 0px 4px 12px rgba(0, 0, 0, 0.05);
}

.category-icon {
  width: 50px;
  height: 50px;
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
  margin-right: 1rem;
}

.category-icon i {
  font-size: 1.2rem;
  color: white;
}

.transport {
  background-color: #4A90E2;
}

.home {
  background-color: #50E3C2;
}

.food {
  background-color: #F5A623;
}

.shopping {
  background-color: #BD10E0;
}

.category-info {
  flex: 1;
}

.category-header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-bottom: 0.5rem;
}

.category-header h3 {
  font-size: 1rem;
  margin-bottom: 0;
}

.category-value {
  font-weight: bold;
  font-size: 0.9rem;
}

.category-progress {
  height: 6px;
  background-color: #F5F8F7;
  border-radius: 3px;
}

.category-progress .progress-bar {
  height: 100%;
  border-radius: 3px;
  background-color: #2B9B7E;
}

.section-header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-bottom: 1rem;
}

.add-activity {
  padding: 0.5rem 1rem;
  font-size: 0.9rem;
}

.add-activity i {
  margin-right: 0.5rem;
}

.activities-list {
  display: flex;
  flex-direction: column;
  gap: 1rem;
}

.activity-item {
  display: flex;
  background-color: white;
  border-radius: 10px;
  padding: 1rem;
  box-shadow: 0px 4px 12px rgba(0, 0, 0, 0.05);
}

.activity-icon {
  min-width: 40px;
  height: 40px;
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
  margin-right: 1rem;
}

.activity-details {
  flex: 1;
}

.activity-main {
  display: flex;
  justify-content: space-between;
  margin-bottom: 0.5rem;
}

.activity-main h4 {
  font-size: 1rem;
  margin-bottom: 0;
}

.activity-impact {
  font-weight: bold;
  color: #E74C3C;
}

.activity-impact.positive {
  color: #2B9B7E;
}

.activity-meta {
  display: flex;
  justify-content: space-between;
  font-size: 0.8rem;
  color: #6A8D87;
}
</style> 
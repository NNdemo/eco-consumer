<template>
  <div class="challenges-container">
    <header class="challenges-header">
      <h1>Challenges</h1>
      <div class="filter-buttons">
        <button class="filter-btn active">All</button>
        <button class="filter-btn">Active</button>
        <button class="filter-btn">Completed</button>
      </div>
    </header>

    <!-- Active Challenge -->
    <section class="active-challenge">
      <h2>Your Active Challenge</h2>
      <div class="challenge-card active">
        <div class="challenge-header">
          <div class="challenge-icon">
            <i class="fas fa-tint-slash"></i>
          </div>
          <div class="challenge-title">
            <h3>Water Saver</h3>
            <div class="challenge-meta">
              <span class="days-left">4 days left</span>
              <span class="participants"><i class="fas fa-users"></i> 120 participants</span>
            </div>
          </div>
        </div>
        <div class="challenge-progress">
          <div class="progress-text">
            <span>Progress: 3/7 days</span>
            <span>43%</span>
          </div>
          <div class="progress-bar-container">
            <div class="progress-bar" style="width: 43%;"></div>
          </div>
        </div>
        <p class="challenge-description">Save water by taking shorter showers, turning off the tap when brushing teeth, and fixing any leaks.</p>
        <div class="challenge-actions">
          <button class="btn btn-primary">Log Today's Action</button>
          <button class="btn btn-secondary">Details</button>
        </div>
      </div>
    </section>

    <!-- Available Challenges -->
    <section class="available-challenges">
      <h2>Available Challenges</h2>
      <div class="challenges-grid">
        <div class="challenge-card">
          <div class="challenge-header">
            <div class="challenge-icon">
              <i class="fas fa-shopping-bag"></i>
            </div>
            <div class="challenge-title">
              <h3>Zero Plastic Shopping</h3>
              <div class="challenge-meta">
                <span class="difficulty">
                  <i class="fas fa-star"></i>
                  <i class="fas fa-star"></i>
                  <i class="far fa-star"></i>
                </span>
                <span class="points">40 pts</span>
              </div>
            </div>
          </div>
          <p class="challenge-description">Shop without using any plastic bags or packaging for a week.</p>
          <div class="challenge-actions">
            <button class="btn btn-primary">Start</button>
          </div>
        </div>

        <div class="challenge-card">
          <div class="challenge-header">
            <div class="challenge-icon">
              <i class="fas fa-bicycle"></i>
            </div>
            <div class="challenge-title">
              <h3>Car-Free Week</h3>
              <div class="challenge-meta">
                <span class="difficulty">
                  <i class="fas fa-star"></i>
                  <i class="fas fa-star"></i>
                  <i class="fas fa-star"></i>
                </span>
                <span class="points">75 pts</span>
              </div>
            </div>
          </div>
          <p class="challenge-description">Use only public transport, cycling, or walking for an entire week.</p>
          <div class="challenge-actions">
            <button class="btn btn-primary">Start</button>
          </div>
        </div>

        <div class="challenge-card">
          <div class="challenge-header">
            <div class="challenge-icon">
              <i class="fas fa-seedling"></i>
            </div>
            <div class="challenge-title">
              <h3>Plant-Based Days</h3>
              <div class="challenge-meta">
                <span class="difficulty">
                  <i class="fas fa-star"></i>
                  <i class="far fa-star"></i>
                  <i class="far fa-star"></i>
                </span>
                <span class="points">30 pts</span>
              </div>
            </div>
          </div>
          <p class="challenge-description">Eat only plant-based meals for 3 days this week.</p>
          <div class="challenge-actions">
            <button class="btn btn-primary">Start</button>
          </div>
        </div>

        <div class="challenge-card">
          <div class="challenge-header">
            <div class="challenge-icon">
              <i class="fas fa-plug"></i>
            </div>
            <div class="challenge-title">
              <h3>Energy Saver</h3>
              <div class="challenge-meta">
                <span class="difficulty">
                  <i class="fas fa-star"></i>
                  <i class="fas fa-star"></i>
                  <i class="far fa-star"></i>
                </span>
                <span class="points">50 pts</span>
              </div>
            </div>
          </div>
          <p class="challenge-description">Reduce your energy consumption by 20% for a week.</p>
          <div class="challenge-actions">
            <button class="btn btn-primary">Start</button>
          </div>
        </div>
      </div>
    </section>

    <!-- Completed Challenges -->
    <section class="completed-challenges">
      <h2>Completed Challenges</h2>
      <div class="challenges-list">
        <div class="completed-item">
          <div class="completed-header">
            <div class="challenge-icon small">
              <i class="fas fa-recycle"></i>
            </div>
            <div class="completed-info">
              <h4>Recycling Pro</h4>
              <span class="completion-date">Completed on Feb 24</span>
            </div>
          </div>
          <div class="completed-result">
            <span class="badge">
              <i class="fas fa-award"></i> Gold
            </span>
            <span class="points-earned">+60 pts</span>
          </div>
        </div>

        <div class="completed-item">
          <div class="completed-header">
            <div class="challenge-icon small">
              <i class="fas fa-lightbulb"></i>
            </div>
            <div class="completed-info">
              <h4>LED Conversion</h4>
              <span class="completion-date">Completed on Feb 15</span>
            </div>
          </div>
          <div class="completed-result">
            <span class="badge">
              <i class="fas fa-award"></i> Silver
            </span>
            <span class="points-earned">+40 pts</span>
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
.challenges-container {
  padding: 1.5rem;
  padding-bottom: 5rem;
}

.challenges-header {
  margin-bottom: 1.5rem;
}

h1 {
  font-size: 1.5rem;
  margin-bottom: 1rem;
}

.filter-buttons {
  display: flex;
  gap: 0.5rem;
  overflow-x: auto;
  padding-bottom: 0.5rem;
}

.filter-btn {
  background-color: #F5F8F7;
  border: none;
  border-radius: 20px;
  padding: 0.5rem 1rem;
  font-weight: 600;
  color: #6A8D87;
  cursor: pointer;
  white-space: nowrap;
}

.filter-btn.active {
  background-color: #2B9B7E;
  color: white;
}

section {
  margin-bottom: 2rem;
}

h2 {
  font-size: 1.2rem;
  margin-bottom: 1rem;
}

.challenge-card {
  background-color: white;
  border-radius: 12px;
  padding: 1.5rem;
  box-shadow: 0px 4px 12px rgba(0, 0, 0, 0.05);
  margin-bottom: 1rem;
}

.challenge-card.active {
  border: 2px solid #2B9B7E;
  background-color: #F9FEFC;
}

.challenge-header {
  display: flex;
  margin-bottom: 1rem;
}

.challenge-icon {
  min-width: 50px;
  height: 50px;
  border-radius: 50%;
  background-color: #E8F4F1;
  display: flex;
  align-items: center;
  justify-content: center;
  margin-right: 1rem;
}

.challenge-icon i {
  font-size: 1.2rem;
  color: #2B9B7E;
}

.challenge-icon.small {
  min-width: 40px;
  height: 40px;
}

.challenge-icon.small i {
  font-size: 1rem;
}

.challenge-title {
  flex: 1;
}

.challenge-title h3 {
  font-size: 1.1rem;
  margin-bottom: 0.5rem;
}

.challenge-meta {
  display: flex;
  justify-content: space-between;
  color: #6A8D87;
  font-size: 0.85rem;
}

.challenge-progress {
  margin-bottom: 1rem;
}

.progress-text {
  display: flex;
  justify-content: space-between;
  margin-bottom: 0.5rem;
  font-size: 0.9rem;
}

.progress-bar-container {
  height: 8px;
  background-color: #F5F8F7;
  border-radius: 4px;
  overflow: hidden;
}

.progress-bar {
  height: 100%;
  background-color: #2B9B7E;
  border-radius: 4px;
}

.challenge-description {
  color: #4A4A4A;
  font-size: 0.95rem;
  line-height: 1.5;
  margin-bottom: 1.5rem;
}

.challenge-actions {
  display: flex;
  gap: 1rem;
}

.challenges-grid {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 1rem;
}

@media (max-width: 600px) {
  .challenges-grid {
    grid-template-columns: 1fr;
  }
}

.difficulty i {
  color: #F9A826;
  font-size: 0.85rem;
}

.points {
  font-weight: 600;
  color: #2B9B7E;
}

.completed-item {
  display: flex;
  justify-content: space-between;
  align-items: center;
  background-color: white;
  padding: 1rem;
  border-radius: 10px;
  margin-bottom: 0.5rem;
  box-shadow: 0px 2px 6px rgba(0, 0, 0, 0.05);
}

.completed-header {
  display: flex;
  align-items: center;
}

.completed-info h4 {
  font-size: 1rem;
  margin-bottom: 0.2rem;
}

.completion-date {
  font-size: 0.8rem;
  color: #6A8D87;
}

.completed-result {
  text-align: right;
}

.badge {
  display: inline-block;
  background-color: #FEF7E6;
  color: #F9A826;
  padding: 0.3rem 0.6rem;
  border-radius: 20px;
  font-size: 0.8rem;
  font-weight: 600;
  margin-bottom: 0.2rem;
}

.badge i {
  margin-right: 0.2rem;
}

.points-earned {
  display: block;
  color: #2B9B7E;
  font-weight: 600;
}

.participants {
  display: flex;
  align-items: center;
  gap: 0.3rem;
}
</style> 
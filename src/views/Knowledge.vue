<template>
  <div class="knowledge-container">
    <header class="knowledge-header">
      <h1>Knowledge Center</h1>
      <div class="search-container">
        <i class="fas fa-search search-icon"></i>
        <input type="text" placeholder="Search articles..." class="search-input" />
      </div>
    </header>

    <!-- Category Tabs -->
    <div class="category-tabs">
      <div class="category-tab active">All</div>
      <div class="category-tab">Minimalism</div>
      <div class="category-tab">Energy</div>
      <div class="category-tab">Food</div>
      <div class="category-tab">Transport</div>
    </div>

    <!-- Featured Article -->
    <section class="featured-article">
      <div class="featured-card">
        <img src="../assets/images/knowledge.jpg" alt="Sustainable Living" class="featured-image" />
        <div class="featured-overlay">
          <span class="featured-badge">Featured</span>
          <h2>10 Simple Ways to Reduce Your Carbon Footprint</h2>
          <div class="article-meta">
            <span><i class="far fa-clock"></i> 5 min read</span>
            <span><i class="far fa-calendar"></i> Mar 1, 2023</span>
          </div>
        </div>
      </div>
    </section>

    <!-- Article List -->
    <section class="articles-section">
      <h2>Recommended for You</h2>
      <div class="articles-list">
        <div class="article-card">
          <div class="article-image-container">
            <img src="../assets/images/eco_product1.jpg" alt="Sustainable Products" class="article-image" />
            <span class="article-category">Minimalism</span>
          </div>
          <div class="article-content">
            <h3>Living with Less: The Path to Sustainability</h3>
            <p>Discover how minimalism can help reduce your environmental impact and lead to a more fulfilling life.</p>
            <div class="article-footer">
              <span class="reading-time"><i class="far fa-clock"></i> 3 min</span>
              <span class="difficulty beginner">Beginner</span>
            </div>
          </div>
        </div>

        <div class="article-card">
          <div class="article-image-container">
            <img src="../assets/images/eco_product2.jpg" alt="Energy Saving" class="article-image" />
            <span class="article-category">Energy</span>
          </div>
          <div class="article-content">
            <h3>Home Energy Efficiency: A Complete Guide</h3>
            <p>Learn practical tips and strategies to reduce your home energy consumption and lower your bills.</p>
            <div class="article-footer">
              <span class="reading-time"><i class="far fa-clock"></i> 7 min</span>
              <span class="difficulty intermediate">Intermediate</span>
            </div>
          </div>
        </div>

        <div class="article-card">
          <div class="article-image-container">
            <img src="../assets/images/eco_product3.jpg" alt="Sustainable Food" class="article-image" />
            <span class="article-category">Food</span>
          </div>
          <div class="article-content">
            <h3>Sustainable Eating: Plant-Based Diet Benefits</h3>
            <p>Explore the environmental benefits of a plant-based diet and get started with simple recipes.</p>
            <div class="article-footer">
              <span class="reading-time"><i class="far fa-clock"></i> 5 min</span>
              <span class="difficulty beginner">Beginner</span>
            </div>
          </div>
        </div>

        <div class="article-card">
          <div class="article-image-container">
            <img src="../assets/images/challenge.jpg" alt="Zero Waste" class="article-image" />
            <span class="article-category">Lifestyle</span>
          </div>
          <div class="article-content">
            <h3>Zero Waste Lifestyle: Getting Started</h3>
            <p>Begin your journey towards a zero-waste lifestyle with these simple but effective first steps.</p>
            <div class="article-footer">
              <span class="reading-time"><i class="far fa-clock"></i> 4 min</span>
              <span class="difficulty beginner">Beginner</span>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- Quick Resources -->
    <section class="resources-section">
      <h2>Quick Resources</h2>
      <div class="resources-grid">
        <div class="resource-card">
          <div class="resource-icon">
            <i class="fas fa-calculator"></i>
          </div>
          <h3>Carbon Calculators</h3>
          <p>Tools to estimate your carbon footprint</p>
        </div>
        <div class="resource-card">
          <div class="resource-icon">
            <i class="fas fa-book"></i>
          </div>
          <h3>Eco Guides</h3>
          <p>Downloadable guides for green living</p>
        </div>
        <div class="resource-card">
          <div class="resource-icon">
            <i class="fas fa-video"></i>
          </div>
          <h3>Video Tutorials</h3>
          <p>Visual learning for sustainable practices</p>
        </div>
        <div class="resource-card">
          <div class="resource-icon">
            <i class="fas fa-link"></i>
          </div>
          <h3>Useful Links</h3>
          <p>Curated resources from around the web</p>
        </div>
      </div>
    </section>
  </div>
</template>

<script setup>
// Static data for demo
</script>

<style scoped>
.knowledge-container {
  padding: 1.5rem;
  padding-bottom: 5rem;
}

.knowledge-header {
  margin-bottom: 1.5rem;
}

h1 {
  font-size: 1.5rem;
  margin-bottom: 1rem;
}

.search-container {
  position: relative;
}

.search-input {
  width: 100%;
  padding: 0.8rem 1rem 0.8rem 2.5rem;
  border: none;
  border-radius: 8px;
  background-color: #F5F8F7;
  font-size: 0.9rem;
}

.search-icon {
  position: absolute;
  left: 1rem;
  top: 50%;
  transform: translateY(-50%);
  color: #6A8D87;
}

.category-tabs {
  display: flex;
  overflow-x: auto;
  gap: 1rem;
  margin-bottom: 1.5rem;
  padding-bottom: 0.5rem;
}

.category-tab {
  white-space: nowrap;
  padding: 0.6rem 1.2rem;
  background-color: #F5F8F7;
  border-radius: 20px;
  font-size: 0.9rem;
  font-weight: 600;
  color: #6A8D87;
  cursor: pointer;
}

.category-tab.active {
  background-color: #2B9B7E;
  color: white;
}

.featured-article {
  margin-bottom: 2rem;
}

.featured-card {
  position: relative;
  border-radius: 12px;
  overflow: hidden;
  height: 200px;
  box-shadow: 0px 4px 12px rgba(0, 0, 0, 0.1);
}

.featured-image {
  width: 100%;
  height: 100%;
  object-fit: cover;
}

.featured-overlay {
  position: absolute;
  bottom: 0;
  left: 0;
  right: 0;
  padding: 1.5rem;
  background: linear-gradient(to top, rgba(0, 0, 0, 0.8), transparent);
  color: white;
}

.featured-badge {
  position: absolute;
  top: 1rem;
  right: 1rem;
  background-color: #2B9B7E;
  color: white;
  padding: 0.3rem 0.8rem;
  border-radius: 20px;
  font-size: 0.8rem;
  font-weight: 600;
}

.featured-overlay h2 {
  margin-bottom: 0.5rem;
  font-size: 1.2rem;
}

.article-meta {
  display: flex;
  gap: 1rem;
  font-size: 0.8rem;
}

.article-meta i {
  margin-right: 0.3rem;
}

.articles-section, .resources-section {
  margin-bottom: 2rem;
}

h2 {
  font-size: 1.2rem;
  margin-bottom: 1rem;
}

.articles-list {
  display: flex;
  flex-direction: column;
  gap: 1rem;
}

.article-card {
  background-color: white;
  border-radius: 12px;
  overflow: hidden;
  box-shadow: 0px 4px 12px rgba(0, 0, 0, 0.05);
}

.article-image-container {
  position: relative;
  height: 150px;
}

.article-image {
  width: 100%;
  height: 100%;
  object-fit: cover;
}

.article-category {
  position: absolute;
  top: 1rem;
  left: 1rem;
  background-color: rgba(43, 155, 126, 0.9);
  color: white;
  padding: 0.3rem 0.8rem;
  border-radius: 20px;
  font-size: 0.8rem;
  font-weight: 600;
}

.article-content {
  padding: 1rem;
}

.article-content h3 {
  font-size: 1.1rem;
  margin-bottom: 0.5rem;
}

.article-content p {
  color: #6A8D87;
  font-size: 0.9rem;
  margin-bottom: 1rem;
  line-height: 1.4;
}

.article-footer {
  display: flex;
  justify-content: space-between;
  font-size: 0.8rem;
}

.reading-time {
  color: #6A8D87;
}

.difficulty {
  padding: 0.2rem 0.6rem;
  border-radius: 20px;
  font-weight: 600;
}

.beginner {
  background-color: #E8F4F1;
  color: #2B9B7E;
}

.intermediate {
  background-color: #FEF7E6;
  color: #F9A826;
}

.advanced {
  background-color: #FEECEC;
  color: #E74C3C;
}

.resources-grid {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 1rem;
}

.resource-card {
  background-color: white;
  border-radius: 12px;
  padding: 1.5rem;
  box-shadow: 0px 4px 12px rgba(0, 0, 0, 0.05);
  text-align: center;
}

.resource-icon {
  width: 50px;
  height: 50px;
  background-color: #E8F4F1;
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
  margin: 0 auto 1rem;
}

.resource-icon i {
  font-size: 1.2rem;
  color: #2B9B7E;
}

.resource-card h3 {
  font-size: 1rem;
  margin-bottom: 0.5rem;
}

.resource-card p {
  font-size: 0.85rem;
  color: #6A8D87;
}
</style> 
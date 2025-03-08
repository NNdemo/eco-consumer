<template>
  <div class="quiz-container">
    <div class="quiz-header">
      <div class="progress-container">
        <div class="progress-bar" :style="{ width: `${(currentQuestion + 1) / questions.length * 100}%` }"></div>
      </div>
      <div class="progress-text">Question {{ currentQuestion + 1 }} of {{ questions.length }}</div>
    </div>

    <div class="question-container" v-if="!quizComplete">
      <h2>{{ questions[currentQuestion].question }}</h2>
      <div class="options-container">
        <div 
          v-for="(option, index) in questions[currentQuestion].options" 
          :key="index"
          class="option"
          :class="{ selected: selectedOption === index }"
          @click="selectOption(index)"
        >
          <div class="option-content">
            <div class="option-text">{{ option.text }}</div>
            <i :class="option.icon"></i>
          </div>
        </div>
      </div>

      <div class="navigation-buttons">
        <button 
          class="btn btn-secondary"
          :disabled="currentQuestion === 0"
          @click="previousQuestion"
        >
          Previous
        </button>
        <button 
          class="btn btn-primary"
          :disabled="selectedOption === null"
          @click="nextQuestion"
        >
          {{ currentQuestion === questions.length - 1 ? 'Finish' : 'Next' }}
        </button>
      </div>
    </div>

    <div class="results-container" v-else>
      <h2>Your Sustainability Profile</h2>
      <div class="profile-summary">
        <div class="profile-icon">
          <i class="fas fa-leaf"></i>
        </div>
        <h3>Eco Enthusiast</h3>
        <p>You're on your way to a more sustainable lifestyle! We've created personalized recommendations to help you continue your journey.</p>
      </div>

      <div class="areas-improvement">
        <h3>Your Focus Areas</h3>
        <div class="area-item">
          <i class="fas fa-utensils"></i>
          <div class="area-content">
            <h4>Sustainable Diet</h4>
            <p>Try reducing meat consumption and buying local produce</p>
          </div>
        </div>
        <div class="area-item">
          <i class="fas fa-shopping-bag"></i>
          <div class="area-content">
            <h4>Mindful Shopping</h4>
            <p>Choose eco-friendly products and reduce packaging waste</p>
          </div>
        </div>
      </div>

      <router-link to="/home" class="btn btn-primary continue-btn">
        Continue to Dashboard
      </router-link>
    </div>
  </div>
</template>

<script setup>
import { ref } from 'vue';

const currentQuestion = ref(0);
const selectedOption = ref(null);
const quizComplete = ref(false);

const questions = [
  {
    question: "How often do you recycle?",
    options: [
      { text: "Always", icon: "fas fa-recycle" },
      { text: "Sometimes", icon: "fas fa-recycle" },
      { text: "Rarely", icon: "fas fa-trash" },
      { text: "Never", icon: "fas fa-trash" }
    ]
  },
  {
    question: "How do you usually commute?",
    options: [
      { text: "Public transport", icon: "fas fa-bus" },
      { text: "Car", icon: "fas fa-car" },
      { text: "Bicycle/Walking", icon: "fas fa-bicycle" },
      { text: "Mix of methods", icon: "fas fa-random" }
    ]
  },
  {
    question: "How often do you eat meat?",
    options: [
      { text: "Daily", icon: "fas fa-drumstick-bite" },
      { text: "Few times a week", icon: "fas fa-drumstick-bite" },
      { text: "Rarely", icon: "fas fa-carrot" },
      { text: "I'm vegetarian/vegan", icon: "fas fa-seedling" }
    ]
  },
  {
    question: "Do you consider sustainability when shopping?",
    options: [
      { text: "Always", icon: "fas fa-leaf" },
      { text: "Sometimes", icon: "fas fa-shopping-bag" },
      { text: "Rarely", icon: "fas fa-shopping-cart" },
      { text: "Never", icon: "fas fa-shopping-cart" }
    ]
  },
  {
    question: "What's your top sustainability goal?",
    options: [
      { text: "Reduce waste", icon: "fas fa-trash-alt" },
      { text: "Save energy", icon: "fas fa-bolt" },
      { text: "Eco-friendly products", icon: "fas fa-shopping-bag" },
      { text: "Sustainable diet", icon: "fas fa-apple-alt" }
    ]
  }
];

const selectOption = (index) => {
  selectedOption.value = index;
};

const nextQuestion = () => {
  if (currentQuestion.value < questions.length - 1) {
    currentQuestion.value++;
    selectedOption.value = null;
  } else {
    // Quiz completed
    quizComplete.value = true;
  }
};

const previousQuestion = () => {
  if (currentQuestion.value > 0) {
    currentQuestion.value--;
    selectedOption.value = null;
  }
};
</script>

<style scoped>
.quiz-container {
  padding: 1.5rem;
  min-height: 100vh;
  display: flex;
  flex-direction: column;
}

.quiz-header {
  margin-bottom: 2rem;
}

.progress-container {
  background-color: #E8F4F1;
  height: 8px;
  border-radius: 4px;
  margin-bottom: 0.5rem;
}

.progress-bar {
  height: 100%;
  background-color: #2B9B7E;
  border-radius: 4px;
  transition: width 0.3s ease;
}

.progress-text {
  text-align: right;
  font-size: 0.9rem;
  color: #6A8D87;
}

.question-container h2 {
  margin-bottom: 2rem;
  text-align: center;
  font-size: 1.5rem;
}

.options-container {
  margin-bottom: 2rem;
}

.option {
  background-color: #F5F8F7;
  border: 2px solid #E8F4F1;
  border-radius: 10px;
  padding: 1rem;
  margin-bottom: 1rem;
  cursor: pointer;
  transition: all 0.2s ease;
}

.option:hover {
  border-color: #2B9B7E;
}

.option.selected {
  border-color: #2B9B7E;
  background-color: #E8F4F1;
}

.option-content {
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.option-text {
  font-weight: 500;
}

.option i {
  font-size: 1.2rem;
  color: #2B9B7E;
}

.navigation-buttons {
  display: flex;
  justify-content: space-between;
}

.results-container {
  text-align: center;
}

.profile-summary {
  background-color: #E8F4F1;
  border-radius: 12px;
  padding: 2rem;
  margin: 1.5rem 0;
}

.profile-icon {
  background-color: #2B9B7E;
  width: 60px;
  height: 60px;
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
  margin: 0 auto 1rem;
}

.profile-icon i {
  font-size: 1.8rem;
  color: white;
}

.areas-improvement {
  margin: 2rem 0;
  text-align: left;
}

.area-item {
  display: flex;
  margin-bottom: 1.5rem;
  align-items: flex-start;
}

.area-item i {
  background-color: #E8F4F1;
  width: 40px;
  height: 40px;
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
  margin-right: 1rem;
  color: #2B9B7E;
}

.area-content h4 {
  margin-bottom: 0.5rem;
}

.continue-btn {
  width: 100%;
  margin-top: 1rem;
}
</style> 
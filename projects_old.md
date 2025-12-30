---
layout: default
title: Projects
permalink: /projects/
---

<div class="projects-hero">
  <div class="hero-content">
    <h1 class="hero-title">My Projects</h1>
    <p class="hero-subtitle">A collection of machine learning, data science, and software engineering projects showcasing my technical expertise and problem-solving abilities.</p>
  </div>
</div>

<style>
.projects-hero {
  background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
  color: white;
  padding: 4rem 2rem;
  margin: -2rem -2rem 3rem -2rem;
  text-align: center;
}

.hero-content {
  max-width: 800px;
  margin: 0 auto;
}

.hero-title {
  font-size: 3rem;
  font-weight: 700;
  margin-bottom: 1rem;
  letter-spacing: -0.5px;
}

.hero-subtitle {
  font-size: 1.2rem;
  font-weight: 300;
  line-height: 1.6;
  opacity: 0.95;
}

.section-title {
  font-size: 2rem;
  font-weight: 700;
  margin: 3rem 0 2rem 0;
  color: #2c3e50;
  border-bottom: 3px solid #667eea;
  padding-bottom: 0.5rem;
  display: inline-block;
}

.projects-grid {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(320px, 1fr));
  gap: 2rem;
  margin-bottom: 3rem;
}

.featured-grid {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(350px, 1fr));
  gap: 2.5rem;
  margin-bottom: 4rem;
}

.project-card {
  background: white;
  border: 1px solid #e1e8ed;
  border-radius: 12px;
  padding: 2rem;
  transition: all 0.3s ease;
  box-shadow: 0 2px 8px rgba(0,0,0,0.05);
}

.project-card:hover {
  transform: translateY(-5px);
  box-shadow: 0 8px 24px rgba(0,0,0,0.12);
  border-color: #667eea;
}

.project-card.featured {
  background: linear-gradient(135deg, #f8f9ff 0%, #fff 100%);
  border: 2px solid #667eea;
}

.project-header {
  display: flex;
  align-items: center;
  gap: 1rem;
  margin-bottom: 1rem;
}

.project-icon {
  font-size: 2rem;
}

.project-title {
  font-size: 1.4rem;
  font-weight: 600;
  color: #2c3e50;
  margin: 0;
}

.project-description {
  color: #555;
  line-height: 1.6;
  margin-bottom: 1rem;
}

.project-tech {
  display: flex;
  flex-wrap: wrap;
  gap: 0.5rem;
  margin-bottom: 1rem;
}

.tech-tag {
  background: #667eea;
  color: white;
  padding: 0.3rem 0.8rem;
  border-radius: 20px;
  font-size: 0.85rem;
  font-weight: 500;
}

.project-links {
  display: flex;
  gap: 1rem;
  margin-top: 1.5rem;
}

.project-link {
  padding: 0.6rem 1.2rem;
  border-radius: 6px;
  text-decoration: none;
  font-weight: 500;
  transition: all 0.2s ease;
  display: inline-block;
}

.project-link.primary {
  background: #667eea;
  color: white;
}

.project-link.primary:hover {
  background: #5568d3;
}

.project-link.secondary {
  background: #f0f2f5;
  color: #2c3e50;
}

.project-link.secondary:hover {
  background: #e1e8ed;
}

.stats-section {
  background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
  color: white;
  padding: 3rem 2rem;
  border-radius: 12px;
  margin: 4rem 0;
  text-align: center;
}

.stats-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
  gap: 2rem;
  margin-top: 2rem;
}

.stat-item {
  padding: 1.5rem;
  background: rgba(255,255,255,0.1);
  border-radius: 8px;
  backdrop-filter: blur(10px);
}

.stat-number {
  font-size: 2.5rem;
  font-weight: 700;
  display: block;
  margin-bottom: 0.5rem;
}

.stat-label {
  font-size: 1rem;
  opacity: 0.9;
}

@media (max-width: 768px) {
  .hero-title {
    font-size: 2rem;
  }
  
  .hero-subtitle {
    font-size: 1rem;
  }
  
  .projects-grid,
  .featured-grid {
    grid-template-columns: 1fr;
  }
}
</style>

## Featured Projects

<div class="featured-grid">
  
  <div class="project-card featured">
    <div class="project-header">
      <span class="project-icon">🏆</span>
      <h3 class="project-title">Quantathon Trading Strategy</h3>
    </div>
    <p class="project-description">
      Developed a sophisticated trading strategy for WBS Quantathon 2024, achieving 3rd place. Implemented advanced statistical analysis and machine learning techniques for market prediction and portfolio optimization.
    </p>
    <div class="project-tech">
      <span class="tech-tag">Python</span>
      <span class="tech-tag">Pandas</span>
      <span class="tech-tag">NumPy</span>
      <span class="tech-tag">Machine Learning</span>
      <span class="tech-tag">Finance</span>
    </div>
    <div class="project-links">
      <a href="https://github.com/ChantelleAA/Quantathon" class="project-link primary">View on GitHub</a>
    </div>
  </div>

  <div class="project-card featured">
    <div class="project-header">
      <span class="project-icon">🧠</span>
      <h3 class="project-title">Brain Tumor Segmentation</h3>
    </div>
    <p class="project-description">
      Deep learning solution for medical image segmentation using U-Net architecture. Achieved high accuracy in identifying and segmenting brain tumors from MRI scans, with potential applications in clinical diagnosis.
    </p>
    <div class="project-tech">
      <span class="tech-tag">Python</span>
      <span class="tech-tag">TensorFlow</span>
      <span class="tech-tag">Keras</span>
      <span class="tech-tag">Computer Vision</span>
      <span class="tech-tag">Medical AI</span>
    </div>
    <div class="project-links">
      <a href="https://github.com/ChantelleAA/brain-tumor-segmentation" class="project-link primary">View on GitHub</a>
    </div>
  </div>

  <div class="project-card featured">
    <div class="project-header">
      <span class="project-icon">💬</span>
      <h3 class="project-title">TLR Helper</h3>
    </div>
    <p class="project-description">
      AI-powered Telegram bot using RAG (Retrieval-Augmented Generation) to assist with university-related questions. Leverages GPT-4 and vector databases for accurate, context-aware responses to student queries.
    </p>
    <div class="project-tech">
      <span class="tech-tag">Python</span>
      <span class="tech-tag">LangChain</span>
      <span class="tech-tag">OpenAI</span>
      <span class="tech-tag">Telegram Bot</span>
      <span class="tech-tag">RAG</span>
    </div>
    <div class="project-links">
      <a href="https://github.com/ChantelleAA/tlr-helper" class="project-link primary">View on GitHub</a>
    </div>
  </div>

</div>

## Machine Learning & AI

<div class="projects-grid">

  <div class="project-card">
    <div class="project-header">
      <span class="project-icon">🤖</span>
      <h3 class="project-title">Sentiment Analysis Tool</h3>
    </div>
    <p class="project-description">
      Advanced NLP model for analyzing sentiment in text data. Implements transformer-based architectures for high-accuracy classification across multiple sentiment categories.
    </p>
    <div class="project-tech">
      <span class="tech-tag">Python</span>
      <span class="tech-tag">Transformers</span>
      <span class="tech-tag">PyTorch</span>
      <span class="tech-tag">NLP</span>
    </div>
    <div class="project-links">
      <a href="https://github.com/ChantelleAA/sentiment-analysis" class="project-link primary">View Project</a>
    </div>
  </div>

  <div class="project-card">
    <div class="project-header">
      <span class="project-icon">📊</span>
      <h3 class="project-title">Customer Churn Prediction</h3>
    </div>
    <p class="project-description">
      Predictive model to identify customers at risk of churning. Utilizes ensemble methods and feature engineering to achieve high precision and recall in churn detection.
    </p>
    <div class="project-tech">
      <span class="tech-tag">Python</span>
      <span class="tech-tag">Scikit-learn</span>
      <span class="tech-tag">XGBoost</span>
      <span class="tech-tag">Analytics</span>
    </div>
    <div class="project-links">
      <a href="https://github.com/ChantelleAA/churn-prediction" class="project-link primary">View Project</a>
    </div>
  </div>

  <div class="project-card">
    <div class="project-header">
      <span class="project-icon">🖼️</span>
      <h3 class="project-title">Image Classification System</h3>
    </div>
    <p class="project-description">
      CNN-based image classifier trained on large-scale datasets. Implements transfer learning with pre-trained models for efficient and accurate image recognition.
    </p>
    <div class="project-tech">
      <span class="tech-tag">Python</span>
      <span class="tech-tag">TensorFlow</span>
      <span class="tech-tag">CNN</span>
      <span class="tech-tag">Computer Vision</span>
    </div>
    <div class="project-links">
      <a href="https://github.com/ChantelleAA/image-classifier" class="project-link primary">View Project</a>
    </div>
  </div>

</div>

## Data Science & Analytics

<div class="projects-grid">

  <div class="project-card">
    <div class="project-header">
      <span class="project-icon">📈</span>
      <h3 class="project-title">Sales Forecasting Dashboard</h3>
    </div>
    <p class="project-description">
      Interactive dashboard for sales forecasting using time series analysis. Provides actionable insights through visualizations and predictive models.
    </p>
    <div class="project-tech">
      <span class="tech-tag">Python</span>
      <span class="tech-tag">Streamlit</span>
      <span class="tech-tag">Prophet</span>
      <span class="tech-tag">Time Series</span>
    </div>
    <div class="project-links">
      <a href="https://github.com/ChantelleAA/sales-forecasting" class="project-link primary">View Project</a>
    </div>
  </div>

  <div class="project-card">
    <div class="project-header">
      <span class="project-icon">🔍</span>
      <h3 class="project-title">A/B Testing Framework</h3>
    </div>
    <p class="project-description">
      Statistical framework for designing and analyzing A/B tests. Includes power analysis, sample size calculation, and comprehensive statistical testing.
    </p>
    <div class="project-tech">
      <span class="tech-tag">Python</span>
      <span class="tech-tag">SciPy</span>
      <span class="tech-tag">Statistics</span>
      <span class="tech-tag">Analytics</span>
    </div>
    <div class="project-links">
      <a href="https://github.com/ChantelleAA/ab-testing" class="project-link primary">View Project</a>
    </div>
  </div>

  <div class="project-card">
    <div class="project-header">
      <span class="project-icon">💹</span>
      <h3 class="project-title">Market Analysis Tool</h3>
    </div>
    <p class="project-description">
      Comprehensive tool for analyzing market trends and patterns. Combines technical indicators with fundamental analysis for informed decision-making.
    </p>
    <div class="project-tech">
      <span class="tech-tag">Python</span>
      <span class="tech-tag">Pandas</span>
      <span class="tech-tag">Plotly</span>
      <span class="tech-tag">Finance</span>
    </div>
    <div class="project-links">
      <a href="https://github.com/ChantelleAA/market-analysis" class="project-link primary">View Project</a>
    </div>
  </div>

</div>

## Web Development & Software Engineering

<div class="projects-grid">

  <div class="project-card">
    <div class="project-header">
      <span class="project-icon">🌐</span>
      <h3 class="project-title">Portfolio Website</h3>
    </div>
    <p class="project-description">
      Personal portfolio website built with modern web technologies. Features responsive design, smooth animations, and optimized performance.
    </p>
    <div class="project-tech">
      <span class="tech-tag">HTML</span>
      <span class="tech-tag">CSS</span>
      <span class="tech-tag">JavaScript</span>
      <span class="tech-tag">Jekyll</span>
    </div>
    <div class="project-links">
      <a href="https://github.com/ChantelleAA/ChantelleAA.github.io" class="project-link primary">View Project</a>
      <a href="https://chantelleaa.github.io" class="project-link secondary">Live Demo</a>
    </div>
  </div>

  <div class="project-card">
    <div class="project-header">
      <span class="project-icon">⚙️</span>
      <h3 class="project-title">API Development</h3>
    </div>
    <p class="project-description">
      RESTful API built with FastAPI for serving machine learning models. Includes authentication, rate limiting, and comprehensive documentation.
    </p>
    <div class="project-tech">
      <span class="tech-tag">Python</span>
      <span class="tech-tag">FastAPI</span>
      <span class="tech-tag">PostgreSQL</span>
      <span class="tech-tag">Docker</span>
    </div>
    <div class="project-links">
      <a href="https://github.com/ChantelleAA/ml-api" class="project-link primary">View Project</a>
    </div>
  </div>

  <div class="project-card">
    <div class="project-header">
      <span class="project-icon">🔧</span>
      <h3 class="project-title">Data Pipeline Automation</h3>
    </div>
    <p class="project-description">
      Automated ETL pipeline for processing large-scale datasets. Implements error handling, monitoring, and scalable architecture for production use.
    </p>
    <div class="project-tech">
      <span class="tech-tag">Python</span>
      <span class="tech-tag">Apache Airflow</span>
      <span class="tech-tag">AWS</span>
      <span class="tech-tag">SQL</span>
    </div>
    <div class="project-links">
      <a href="https://github.com/ChantelleAA/data-pipeline" class="project-link primary">View Project</a>
    </div>
  </div>

</div>

<div class="stats-section">
  <h2 style="margin-bottom: 0.5rem; font-size: 2rem;">Project Statistics</h2>
  <p style="opacity: 0.9; margin-bottom: 2rem;">A snapshot of my technical journey</p>
  <div class="stats-grid">
    <div class="stat-item">
      <span class="stat-number">15+</span>
      <span class="stat-label">Projects Completed</span>
    </div>
    <div class="stat-item">
      <span class="stat-number">10+</span>
      <span class="stat-label">Technologies Mastered</span>
    </div>
    <div class="stat-item">
      <span class="stat-number">3rd</span>
      <span class="stat-label">Place at WBS Quantathon</span>
    </div>
    <div class="stat-item">
      <span class="stat-number">100%</span>
      <span class="stat-label">Passion for Learning</span>
    </div>
  </div>
</div>

---

<div style="text-align: center; margin-top: 4rem; padding: 2rem; background: #f8f9fa; border-radius: 8px;">
  <p style="font-size: 1.1rem; color: #555; margin-bottom: 1rem;">
    Interested in collaborating or learning more about my work?
  </p>
  <a href="/contact/" style="background: #667eea; color: white; padding: 0.8rem 2rem; border-radius: 6px; text-decoration: none; font-weight: 600; display: inline-block; transition: all 0.2s ease;">
    Get In Touch
  </a>
</div>

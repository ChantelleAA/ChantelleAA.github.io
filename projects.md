---
layout: default
title: Projects
permalink: /projects/
---

<div class="projects-hero">
  <div class="hero-content">
    <h1 class="hero-title">My Projects</h1>
    <p class="hero-subtitle">From climate AI research to production ML systems for education, healthcare, and environmental monitoring. Building technology that solves real-world problems.</p>
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
  grid-template-columns: repeat(3, 1fr);
  gap: 2rem;
  margin-bottom: 3rem;
}

@media (max-width: 1200px) {
  .projects-grid {
    grid-template-columns: repeat(2, 1fr);
  }
}

@media (max-width: 768px) {
  .projects-grid {
    grid-template-columns: 1fr;
  }
}

.project-card {
  background: white;
  border: 2px solid #e1e8ed;
  border-radius: 12px;
  padding: 2rem;
  transition: all 0.3s ease;
  box-shadow: 0 2px 8px rgba(0,0,0,0.05);
  display: flex;
  flex-direction: column;
}

.project-card:hover {
  transform: translateY(-5px);
  box-shadow: 0 8px 24px rgba(0,0,0,0.12);
  border-color: #667eea;
}

.project-header {
  display: flex;
  align-items: flex-start;
  justify-content: space-between;
  margin-bottom: 1rem;
}

.project-icon {
  font-size: 2rem;
  margin-right: 0.5rem;
}

.project-badge {
  padding: 0.25rem 0.75rem;
  background: #667eea;
  color: white;
  border-radius: 20px;
  font-size: 0.75rem;
  font-weight: 600;
  text-transform: uppercase;
  letter-spacing: 0.5px;
}

.project-badge.award { background: linear-gradient(135deg, #f093fb, #f5576c); }
.project-badge.research { background: linear-gradient(135deg, #4facfe, #00f2fe); }
.project-badge.education { background: linear-gradient(135deg, #43e97b, #38f9d7); }
.project-badge.production { background: linear-gradient(135deg, #fa709a, #fee140); }

.project-title {
  font-size: 1.4rem;
  font-weight: 600;
  color: #2c3e50;
  margin: 0 0 1rem 0;
  line-height: 1.3;
}

.project-description {
  color: #555;
  line-height: 1.6;
  margin-bottom: 1rem;
  flex-grow: 1;
}

.project-tech {
  display: flex;
  flex-wrap: wrap;
  gap: 0.5rem;
  margin-bottom: 1rem;
}

.tech-tag {
  background: #2c3e50;
  color: white;
  padding: 0.3rem 0.8rem;
  border-radius: 20px;
  font-size: 0.85rem;
  font-weight: 500;
}

.project-links {
  display: flex;
  gap: 1rem;
  margin-top: auto;
  padding-top: 1rem;
  border-top: 1px solid #e1e8ed;
}

.project-link {
  padding: 0.6rem 1.2rem;
  border-radius: 6px;
  text-decoration: none;
  font-weight: 500;
  transition: all 0.2s ease;
  display: inline-flex;
  align-items: center;
  gap: 0.5rem;
  font-size: 0.9rem;
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

.project-meta {
  font-size: 0.85rem;
  color: #888;
  display: flex;
  align-items: center;
  gap: 0.5rem;
}

.impact-highlight {
  background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
  color: white;
  padding: 0.4rem 0.8rem;
  border-radius: 6px;
  font-size: 0.9rem;
  font-weight: 600;
  display: inline-block;
  margin-top: 0.5rem;
}

@media (max-width: 768px) {
  .hero-title {
    font-size: 2rem;
  }
  
  .hero-subtitle {
    font-size: 1rem;
  }
  
  .projects-grid {
    grid-template-columns: 1fr;
  }
}
</style>

## Featured Projects

<div class="projects-grid">
  
  <div class="project-card">
    <div class="project-header">
      <span class="project-icon">🏆</span>
      <span class="project-badge award">Award-Winning</span>
    </div>
    <h3 class="project-title">Quantathon Judging Platform</h3>
    <p class="project-description">
      Full judging and scoring platform for AIMS Quantathon hackathon. Real-time leaderboards, expertise-based criteria weighting, secure one-time voting links, and automated scoring. Successfully deployed for multi-day hackathon event.
    </p>
    <div class="project-tech">
      <span class="tech-tag">Django</span>
      <span class="tech-tag">PostgreSQL</span>
      <span class="tech-tag">HTMX</span>
      <span class="tech-tag">Bootstrap</span>
    </div>
    <div class="project-links">
      <a href="https://github.com/ChantelleAA/judging_criteria" class="project-link primary" target="_blank" rel="noopener">
        <i class="fa-brands fa-github"></i> View Code
      </a>
      <span class="project-meta"><i class="fa-solid fa-calendar"></i> Jul 2025</span>
    </div>
  </div>

  <div class="project-card">
    <div class="project-header">
      <span class="project-icon">📚</span>
      <span class="project-badge education">Education</span>
    </div>
    <h3 class="project-title">TLR Helper – Ghana Curriculum Platform</h3>
    <p class="project-description">
      Web application for Ghana's Standards-Based Curriculum that suggests teaching resources by class, strand, indicator, special needs accommodations, and learning styles. Used in TEDD Ghana teacher training workshops.
    </p>
    <div class="project-tech">
      <span class="tech-tag">Django</span>
      <span class="tech-tag">HTMX</span>
      <span class="tech-tag">Bootstrap</span>
      <span class="tech-tag">SQLite</span>
    </div>
    <div class="project-links">
      <a href="https://github.com/ChantelleAA/tlr_app" class="project-link primary" target="_blank" rel="noopener">
        <i class="fa-brands fa-github"></i> View Code
      </a>
    </div>
  </div>

  <div class="project-card">
    <div class="project-header">
      <span class="project-icon">🧠</span>
      <span class="project-badge research">Research</span>
    </div>
    <h3 class="project-title">Brain Tumor Segmentation on Sub-Saharan MRI</h3>
    <p class="project-description">
      Ensemble deep learning methods for medical imaging on limited datasets. MICCAI 2023 scholarship recipient. Improving healthcare AI for resource-constrained settings with U-Net and attention mechanisms.
    </p>
    <div class="impact-highlight">
      <i class="fa-solid fa-award"></i> MICCAI 2023 Scholar
    </div>
    <div class="project-tech">
      <span class="tech-tag">PyTorch</span>
      <span class="tech-tag">Medical Imaging</span>
      <span class="tech-tag">U-Net</span>
      <span class="tech-tag">Ensemble ML</span>
    </div>
    <div class="project-links">
      <a href="https://arxiv.org/abs/2508.10905" class="project-link primary" target="_blank" rel="noopener">
        <i class="fa-solid fa-file-pdf"></i> Read Paper
      </a>
    </div>
  </div>

  <div class="project-card">
    <div class="project-header">
      <span class="project-icon">🌍</span>
      <span class="project-badge research">Research</span>
    </div>
    <h3 class="project-title">GeoSeg Biodiversity Segmentation</h3>
    <p class="project-description">
      Geospatial AI combining land cover segmentation with pollution monitoring. Uses Sentinel-5P satellite data and OpenEarthMap for environmental analysis. Achieved 87-90% mIoU improvement over baseline models.
    </p>
    <div class="impact-highlight">
      <i class="fa-solid fa-chart-line"></i> 87-90% mIoU Improvement
    </div>
    <div class="project-tech">
      <span class="tech-tag">PyTorch</span>
      <span class="tech-tag">GeoPandas</span>
      <span class="tech-tag">Sentinel</span>
      <span class="tech-tag">Streamlit</span>
    </div>
    <div class="project-links">
      <a href="https://github.com/ChantelleAA/geoseg" class="project-link primary" target="_blank" rel="noopener">
        <i class="fa-brands fa-github"></i> View Code
      </a>
    </div>
  </div>

</div>

## Research Projects

<div class="projects-grid">

  <div class="project-card">
    <div class="project-header">
      <span class="project-icon">🎮</span>
      <span class="project-badge research">RL/Games</span>
    </div>
    <h3 class="project-title">Oware Nam-nam Reinforcement Learning</h3>
    <p class="project-description">
      DQN, DDQN, A3C, and AlphaZero implementations for traditional African board game. Custom RL environment with self-play training and human-vs-agent modes. LUT Masters thesis project on applying modern RL to cultural games.
    </p>
    <div class="project-tech">
      <span class="tech-tag">Python</span>
      <span class="tech-tag">TensorFlow</span>
      <span class="tech-tag">Stable-Baselines</span>
      <span class="tech-tag">Gym</span>
    </div>
    <div class="project-links">
      <a href="https://github.com/ChantelleAA/Reinforcement_Learning_Oware" class="project-link primary" target="_blank" rel="noopener">
        <i class="fa-brands fa-github"></i> View Code
      </a>
      <a href="https://lutpub.lut.fi/bitstream/handle/10024/167861/mastersthesis_Amoako-Atta_Chantelle.pdf" class="project-link secondary" target="_blank" rel="noopener">
        <i class="fa-solid fa-file-pdf"></i> Thesis
      </a>
    </div>
  </div>

  <div class="project-card">
    <div class="project-header">
      <span class="project-icon">💨</span>
      <span class="project-badge research">Climate</span>
    </div>
    <h3 class="project-title">RTE Pollution Dashboard</h3>
    <p class="project-description">
      Multi-city air quality analytics dashboard using Sentinel-5P satellite data. Real-time monitoring of NO₂, CO, SO₂, and PM2.5 levels across African cities. Interactive visualizations for environmental research and policy.
    </p>
    <div class="project-tech">
      <span class="tech-tag">Python</span>
      <span class="tech-tag">Streamlit</span>
      <span class="tech-tag">Sentinel-5P</span>
      <span class="tech-tag">Pandas</span>
    </div>
    <div class="project-links">
      <a href="https://github.com/ChantelleAA/RTE_pollution_dashboard" class="project-link primary" target="_blank" rel="noopener">
        <i class="fa-brands fa-github"></i> View Code
      </a>
    </div>
  </div>

  <div class="project-card">
    <div class="project-header">
      <span class="project-icon">📝</span>
      <span class="project-badge research">OCR/NLP</span>
    </div>
    <h3 class="project-title">OCR Research & Evaluation</h3>
    <p class="project-description">
      Comprehensive benchmarking of OCR engines (Tesseract, EasyOCR, PaddleOCR) on diverse document types. Performance evaluation framework for text extraction accuracy, speed, and multilingual support in production scenarios.
    </p>
    <div class="project-tech">
      <span class="tech-tag">Python</span>
      <span class="tech-tag">Tesseract</span>
      <span class="tech-tag">EasyOCR</span>
      <span class="tech-tag">Computer Vision</span>
    </div>
    <div class="project-links">
      <a href="https://github.com/ChantelleAA/OCR_research" class="project-link primary" target="_blank" rel="noopener">
        <i class="fa-brands fa-github"></i> View Code
      </a>
    </div>
  </div>

  <div class="project-card">
    <div class="project-header">
      <span class="project-icon">❤️</span>
      <span class="project-badge research">Healthcare</span>
    </div>
    <h3 class="project-title">Cardiac Arrhythmia Classifier</h3>
    <p class="project-description">
      Machine learning algorithms for arrhythmia prediction from physiological signals. AIMS Rwanda MSc thesis project using classical ML and signal processing techniques for healthcare diagnostics in resource-limited settings.
    </p>
    <div class="project-tech">
      <span class="tech-tag">Python</span>
      <span class="tech-tag">Scikit-learn</span>
      <span class="tech-tag">Signal Processing</span>
      <span class="tech-tag">ML</span>
    </div>
    <div class="project-links">
      <a href="https://github.com/ChantelleAA/Cardiac_Arrhythmia_ML" class="project-link primary" target="_blank" rel="noopener">
        <i class="fa-brands fa-github"></i> View Code
      </a>
    </div>
  </div>

  <div class="project-card">
    <div class="project-header">
      <span class="project-icon">✋</span>
      <span class="project-badge research">Computer Vision</span>
    </div>
    <h3 class="project-title">3D LeapMotion Digit Classification</h3>
    <p class="project-description">
      Real-time hand gesture recognition using LeapMotion sensor and deep learning. Achieved 99% accuracy in digit classification from 3D hand poses. Exploration of gesture-based interfaces for accessible computing.
    </p>
    <div class="impact-highlight">
      <i class="fa-solid fa-bullseye"></i> 99% Accuracy
    </div>
    <div class="project-tech">
      <span class="tech-tag">Python</span>
      <span class="tech-tag">TensorFlow</span>
      <span class="tech-tag">LeapMotion</span>
      <span class="tech-tag">3D Vision</span>
    </div>
    <div class="project-links">
      <a href="https://github.com/ChantelleAA/leapmotion_digit_classification" class="project-link primary" target="_blank" rel="noopener">
        <i class="fa-brands fa-github"></i> View Code
      </a>
    </div>
  </div>

</div>

## ML/AI Applications

<div class="projects-grid">

  <div class="project-card">
    <div class="project-header">
      <span class="project-icon">💬</span>
      <span class="project-badge production">Production</span>
    </div>
    <h3 class="project-title">NileEdge AI Assistant</h3>
    <p class="project-description">
      Context-aware chatbot with semantic FAQ matching using ChromaDB vector search and Whisper transcription. Production-ready customer support system with intelligent query routing, multi-language support, and conversation history.
    </p>
    <div class="project-tech">
      <span class="tech-tag">Python</span>
      <span class="tech-tag">Flask</span>
      <span class="tech-tag">ChromaDB</span>
      <span class="tech-tag">Whisper</span>
      <span class="tech-tag">OpenAI</span>
    </div>
    <div class="project-links">
      <a href="https://github.com/ChantelleAA/response_aigent" class="project-link primary" target="_blank" rel="noopener">
        <i class="fa-brands fa-github"></i> View Code
      </a>
    </div>
  </div>

  <div class="project-card">
    <div class="project-header">
      <span class="project-icon">⚖️</span>
      <span class="project-badge award">Hackathon Winner</span>
    </div>
    <h3 class="project-title">Case-Mediators Matching System</h3>
    <p class="project-description">
      Ishango AI Hackathon winning project. Intelligent matching system pairing legal cases with appropriate mediators based on expertise, availability, and case characteristics. Uses NLP for case analysis and optimization algorithms.
    </p>
    <div class="impact-highlight">
      <i class="fa-solid fa-trophy"></i> Ishango AI Hackathon Winner
    </div>
    <div class="project-tech">
      <span class="tech-tag">Python</span>
      <span class="tech-tag">NLP</span>
      <span class="tech-tag">Matching Algorithms</span>
      <span class="tech-tag">Flask</span>
    </div>
    <div class="project-links">
      <a href="https://github.com/ChantelleAA/Case_Mediators_Matching" class="project-link primary" target="_blank" rel="noopener">
        <i class="fa-brands fa-github"></i> View Code
      </a>
    </div>
  </div>

  <div class="project-card">
    <div class="project-header">
      <span class="project-icon">🗳️</span>
      <span class="project-badge research">NLP</span>
    </div>
    <h3 class="project-title">Twitter Election Prediction</h3>
    <p class="project-description">
      BERT and GPT-based sentiment analysis for predicting election outcomes from social media. Achieved 20% accuracy improvement through ensemble methods. Analysis of political discourse and public opinion dynamics on Twitter.
    </p>
    <div class="impact-highlight">
      <i class="fa-solid fa-chart-up"></i> 20% Accuracy Improvement
    </div>
    <div class="project-tech">
      <span class="tech-tag">Python</span>
      <span class="tech-tag">BERT</span>
      <span class="tech-tag">GPT</span>
      <span class="tech-tag">Transformers</span>
    </div>
    <div class="project-links">
      <a href="https://github.com/ChantelleAA/twitter_election_prediction" class="project-link primary" target="_blank" rel="noopener">
        <i class="fa-brands fa-github"></i> View Code
      </a>
    </div>
  </div>

  <div class="project-card">
    <div class="project-header">
      <span class="project-icon">📰</span>
      <span class="project-badge research">NLP</span>
    </div>
    <h3 class="project-title">News Article Political Sentiment</h3>
    <p class="project-description">
      Large-scale sentiment analysis of news articles for political bias detection and framing analysis. Transformer-based models for understanding media narratives and political positioning across multiple news sources.
    </p>
    <div class="project-tech">
      <span class="tech-tag">Python</span>
      <span class="tech-tag">Transformers</span>
      <span class="tech-tag">NLP</span>
      <span class="tech-tag">Sentiment Analysis</span>
    </div>
    <div class="project-links">
      <a href="https://github.com/ChantelleAA/news_sentiment_analysis" class="project-link primary" target="_blank" rel="noopener">
        <i class="fa-brands fa-github"></i> View Code
      </a>
    </div>
  </div>

</div>

## Education & Workshops

<div class="projects-grid">

  <div class="project-card">
    <div class="project-header">
      <span class="project-icon">🛰️</span>
      <span class="project-badge education">Workshop</span>
    </div>
    <h3 class="project-title">GeoAI Workshop Materials</h3>
    <p class="project-description">
      Comprehensive tutorials for satellite imagery processing and geospatial machine learning. Covers Sentinel data access, land cover classification, change detection, and environmental monitoring. Used in multiple workshop sessions.
    </p>
    <div class="project-tech">
      <span class="tech-tag">Python</span>
      <span class="tech-tag">Jupyter</span>
      <span class="tech-tag">GeoPandas</span>
      <span class="tech-tag">Satellite Imagery</span>
    </div>
    <div class="project-links">
      <a href="https://github.com/ChantelleAA/geoai_workshop" class="project-link primary" target="_blank" rel="noopener">
        <i class="fa-brands fa-github"></i> View Materials
      </a>
    </div>
  </div>

  <div class="project-card">
    <div class="project-header">
      <span class="project-icon">🐍</span>
      <span class="project-badge education">Teaching</span>
    </div>
    <h3 class="project-title">Python Learning Materials</h3>
    <p class="project-description">
      Structured teaching notebooks for 200+ students across universities and professional programs. Covers Python fundamentals, data structures, NumPy, Pandas, visualization, and machine learning basics with practical exercises.
    </p>
    <div class="impact-highlight">
      <i class="fa-solid fa-users"></i> 200+ Students Taught
    </div>
    <div class="project-tech">
      <span class="tech-tag">Python</span>
      <span class="tech-tag">Jupyter</span>
      <span class="tech-tag">Pandas</span>
      <span class="tech-tag">Education</span>
    </div>
    <div class="project-links">
      <a href="https://github.com/ChantelleAA/python_teaching_materials" class="project-link primary" target="_blank" rel="noopener">
        <i class="fa-brands fa-github"></i> View Materials
      </a>
    </div>
  </div>

</div>

## Web Applications

<div class="projects-grid">

  <div class="project-card">
    <div class="project-header">
      <span class="project-icon">✈️</span>
      <span class="project-badge">Web App</span>
    </div>
    <h3 class="project-title">Flight Cost Optimization Tool</h3>
    <p class="project-description">
      Web application for finding optimal flight routes and cost savings. Compares direct flights vs. multi-leg connections, analyzes price trends, and suggests best booking times. Helps travelers make informed decisions.
    </p>
    <div class="project-tech">
      <span class="tech-tag">Python</span>
      <span class="tech-tag">Flask</span>
      <span class="tech-tag">APIs</span>
      <span class="tech-tag">Optimization</span>
    </div>
    <div class="project-links">
      <a href="https://github.com/ChantelleAA/flight_optimization" class="project-link primary" target="_blank" rel="noopener">
        <i class="fa-brands fa-github"></i> View Code
      </a>
    </div>
  </div>

  <div class="project-card">
    <div class="project-header">
      <span class="project-icon">📊</span>
      <span class="project-badge">Analytics</span>
    </div>
    <h3 class="project-title">Survey Data Analysis Platform</h3>
    <p class="project-description">
      Interactive platform for survey data exploration and visualization. Automated report generation, statistical analysis, cross-tabulation, and customizable dashboards. Used for research and organizational data analysis.
    </p>
    <div class="project-tech">
      <span class="tech-tag">Python</span>
      <span class="tech-tag">Streamlit</span>
      <span class="tech-tag">Pandas</span>
      <span class="tech-tag">Plotly</span>
    </div>
    <div class="project-links">
      <a href="https://github.com/ChantelleAA/survey_analysis" class="project-link primary" target="_blank" rel="noopener">
        <i class="fa-brands fa-github"></i> View Code
      </a>
    </div>
  </div>

</div>

---

<div style="text-align: center; margin-top: 4rem; padding: 2rem; background: linear-gradient(135deg, #667eea 0%, #764ba2 100%); border-radius: 12px; color: white;">
  <h2 style="margin-bottom: 1rem; font-size: 2rem;">Want to Collaborate?</h2>
  <p style="font-size: 1.1rem; margin-bottom: 1.5rem; opacity: 0.95;">
    I'm always interested in research collaborations, consulting opportunities, and impactful projects.
  </p>
  <a href="mailto:chantelatta@gmail.com" style="background: white; color: #667eea; padding: 0.8rem 2rem; border-radius: 6px; text-decoration: none; font-weight: 600; display: inline-block; transition: all 0.2s ease;">
    Get In Touch
  </a>
</div>

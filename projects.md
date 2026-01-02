---
layout: default
title: Projects
permalink: /projects/
---

<style>
@import url('https://fonts.googleapis.com/css2?family=Crimson+Pro:wght@300;400;600;700&family=DM+Sans:wght@400;500;700&display=swap');

:root {
  --color-cream: #FAF8F5;
  --color-dark: #1A1A1A;
  --color-charcoal: #2D2D2D;
  --color-sage: #7A9D7E;
  --color-sage-dark: #5A7D5E;
  --color-terracotta: #C97B63;
  --color-terracotta-light: #E8B4A3;
  --color-gold: #D4A574;
  --color-gold-light: #E8C9A0;
  --color-border: #E5E1DA;
  --color-text-muted: #666666;
  
  --font-display: 'Crimson Pro', serif;
  --font-body: 'DM Sans', sans-serif;
  
  --shadow-sm: 0 2px 8px rgba(0, 0, 0, 0.04);
  --shadow-md: 0 4px 16px rgba(0, 0, 0, 0.06);
  --shadow-lg: 0 12px 32px rgba(0, 0, 0, 0.08);
}

* {
  box-sizing: border-box;
}

body {
  background: var(--color-cream);
  color: var(--color-dark);
  font-family: var(--font-body);
  line-height: 1.6;
}

/* Hero Section */
.projects-hero {
  background: var(--color-dark);
  color: var(--color-cream);
  padding: 8rem 2rem 6rem;
  margin: -2rem -2rem 5rem -2rem;
  position: relative;
  overflow: hidden;
}

.projects-hero::before {
  content: '';
  position: absolute;
  top: -50%;
  right: -20%;
  width: 600px;
  height: 600px;
  background: radial-gradient(circle, rgba(122, 157, 126, 0.15) 0%, transparent 70%);
  border-radius: 50%;
  animation: float 20s ease-in-out infinite;
}

.projects-hero::after {
  content: '';
  position: absolute;
  bottom: -30%;
  left: -10%;
  width: 500px;
  height: 500px;
  background: radial-gradient(circle, rgba(201, 123, 99, 0.12) 0%, transparent 70%);
  border-radius: 50%;
  animation: float 15s ease-in-out infinite reverse;
}

@keyframes float {
  0%, 100% { transform: translate(0, 0) scale(1); }
  50% { transform: translate(-30px, 30px) scale(1.05); }
}

.hero-content {
  max-width: 900px;
  margin: 0 auto;
  position: relative;
  z-index: 1;
}

.hero-label {
  font-size: 0.875rem;
  font-weight: 500;
  letter-spacing: 2px;
  text-transform: uppercase;
  color: var(--color-gold-light);
  margin-bottom: 1.5rem;
  opacity: 0;
  animation: fadeInUp 0.8s ease-out 0.2s forwards;
}

.hero-title {
  font-family: var(--font-display);
  font-size: 4.5rem;
  font-weight: 600;
  margin-bottom: 1.5rem;
  letter-spacing: -1.5px;
  line-height: 1.1;
  opacity: 0;
  animation: fadeInUp 0.8s ease-out 0.4s forwards;
}

.hero-subtitle {
  font-size: 1.25rem;
  font-weight: 300;
  line-height: 1.8;
  color: rgba(250, 248, 245, 0.85);
  max-width: 700px;
  margin: 0 auto;
  opacity: 0;
  animation: fadeInUp 0.8s ease-out 0.6s forwards;
}

@keyframes fadeInUp {
  from {
    opacity: 0;
    transform: translateY(30px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

/* Filter Section */
.filter-section {
  max-width: 1400px;
  margin: 0 auto 4rem;
  padding: 0 2rem;
  display: flex;
  gap: 1rem;
  flex-wrap: wrap;
  justify-content: center;
}

.filter-btn {
  padding: 0.875rem 2rem;
  border: 1.5px solid var(--color-border);
  background: white;
  color: var(--color-charcoal);
  border-radius: 8px;
  font-family: var(--font-body);
  font-weight: 500;
  font-size: 0.9rem;
  cursor: pointer;
  transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);
  position: relative;
  overflow: hidden;
}

.filter-btn::before {
  content: '';
  position: absolute;
  top: 0;
  left: -100%;
  width: 100%;
  height: 100%;
  background: linear-gradient(90deg, transparent, rgba(122, 157, 126, 0.1), transparent);
  transition: left 0.5s ease;
}

.filter-btn:hover::before {
  left: 100%;
}

.filter-btn:hover {
  border-color: var(--color-sage);
  color: var(--color-sage-dark);
  transform: translateY(-2px);
  box-shadow: var(--shadow-sm);
}

.filter-btn.active {
  background: var(--color-sage);
  color: white;
  border-color: var(--color-sage);
  box-shadow: 0 4px 12px rgba(122, 157, 126, 0.25);
}

/* Projects Grid */
.projects-grid {
  max-width: 1400px;
  margin: 0 auto;
  padding: 0 2rem;
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(450px, 1fr));
  gap: 3rem;
  margin-bottom: 6rem;
}

@media (max-width: 768px) {
  .projects-grid {
    grid-template-columns: 1fr;
    gap: 2.5rem;
  }
}

/* Project Card */
.project-card {
  background: white;
  border-radius: 12px;
  overflow: hidden;
  box-shadow: var(--shadow-sm);
  transition: all 0.5s cubic-bezier(0.4, 0, 0.2, 1);
  position: relative;
  border: 1px solid var(--color-border);
  opacity: 0;
  transform: translateY(30px);
  animation: cardFadeIn 0.6s ease-out forwards;
}

@keyframes cardFadeIn {
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

.project-card:nth-child(1) { animation-delay: 0.1s; }
.project-card:nth-child(2) { animation-delay: 0.15s; }
.project-card:nth-child(3) { animation-delay: 0.2s; }
.project-card:nth-child(4) { animation-delay: 0.25s; }
.project-card:nth-child(5) { animation-delay: 0.3s; }
.project-card:nth-child(6) { animation-delay: 0.35s; }
.project-card:nth-child(7) { animation-delay: 0.4s; }
.project-card:nth-child(8) { animation-delay: 0.45s; }
.project-card:nth-child(9) { animation-delay: 0.5s; }

.project-card:hover {
  transform: translateY(-8px);
  box-shadow: var(--shadow-lg);
  border-color: var(--color-sage);
}

.project-image-wrapper {
  position: relative;
  width: 100%;
  height: 280px;
  overflow: hidden;
  background: linear-gradient(135deg, #F5F3EF 0%, #E8E5DF 100%);
}

.project-image {
  width: 100%;
  height: 100%;
  object-fit: cover;
  transition: transform 0.6s cubic-bezier(0.4, 0, 0.2, 1);
}

.project-card:hover .project-image {
  transform: scale(1.05);
}

.project-category-badge {
  position: absolute;
  top: 1.25rem;
  right: 1.25rem;
  background: rgba(255, 255, 255, 0.95);
  backdrop-filter: blur(10px);
  color: var(--color-charcoal);
  padding: 0.5rem 1.25rem;
  border-radius: 6px;
  font-size: 0.8rem;
  font-weight: 600;
  text-transform: uppercase;
  letter-spacing: 0.5px;
  box-shadow: 0 2px 12px rgba(0, 0, 0, 0.1);
  border: 1px solid rgba(0, 0, 0, 0.05);
}

.project-content {
  padding: 2.25rem;
}

.project-title {
  font-family: var(--font-display);
  font-size: 1.75rem;
  font-weight: 600;
  color: var(--color-dark);
  margin-bottom: 1rem;
  line-height: 1.3;
  display: flex;
  align-items: center;
  gap: 0.75rem;
}

.project-title .emoji {
  font-size: 2rem;
}

.project-description {
  font-size: 1rem;
  line-height: 1.75;
  color: var(--color-text-muted);
  margin-bottom: 1.5rem;
}

.project-description strong {
  color: var(--color-charcoal);
  font-weight: 600;
}

.project-features {
  list-style: none;
  padding: 0;
  margin: 1.5rem 0;
}

.project-features li {
  padding: 0.625rem 0;
  padding-left: 2rem;
  position: relative;
  font-size: 0.95rem;
  color: var(--color-charcoal);
  line-height: 1.6;
}

.project-features li:before {
  content: "→";
  position: absolute;
  left: 0;
  color: var(--color-sage);
  font-weight: bold;
  font-size: 1.1rem;
}

.project-tech {
  display: flex;
  flex-wrap: wrap;
  gap: 0.625rem;
  margin: 1.75rem 0;
  padding-top: 1.75rem;
  border-top: 1px solid var(--color-border);
}

.tech-badge {
  padding: 0.5rem 1rem;
  background: var(--color-cream);
  color: var(--color-charcoal);
  border-radius: 6px;
  font-size: 0.8rem;
  font-weight: 500;
  border: 1px solid var(--color-border);
  transition: all 0.3s ease;
}

.tech-badge:hover {
  background: var(--color-sage);
  color: white;
  border-color: var(--color-sage);
  transform: translateY(-2px);
}

.project-links {
  display: flex;
  gap: 0.875rem;
  flex-wrap: wrap;
  margin-top: 1.75rem;
}

.project-link {
  display: inline-flex;
  align-items: center;
  gap: 0.5rem;
  padding: 0.875rem 1.5rem;
  background: var(--color-sage);
  color: white;
  text-decoration: none;
  border-radius: 8px;
  font-weight: 500;
  font-size: 0.9rem;
  transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);
  border: 1.5px solid var(--color-sage);
}

.project-link:hover {
  background: var(--color-sage-dark);
  border-color: var(--color-sage-dark);
  transform: translateY(-2px);
  box-shadow: 0 4px 12px rgba(122, 157, 126, 0.25);
}

.project-link.secondary {
  background: white;
  color: var(--color-sage);
  border: 1.5px solid var(--color-sage);
}

.project-link.secondary:hover {
  background: var(--color-sage);
  color: white;
}

/* Stats Section */
.projects-stats {
  background: var(--color-dark);
  padding: 5rem 2rem;
  border-radius: 16px;
  margin: 0 2rem 5rem;
  max-width: 1400px;
  margin-left: auto;
  margin-right: auto;
  text-align: center;
  color: var(--color-cream);
  position: relative;
  overflow: hidden;
}

.projects-stats::before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background: 
    linear-gradient(45deg, transparent 48%, rgba(122, 157, 126, 0.05) 50%, transparent 52%),
    linear-gradient(-45deg, transparent 48%, rgba(201, 123, 99, 0.05) 50%, transparent 52%);
  background-size: 40px 40px;
  opacity: 0.5;
}

.projects-stats h2 {
  font-family: var(--font-display);
  font-size: 3rem;
  font-weight: 600;
  margin-bottom: 3.5rem;
  letter-spacing: -0.5px;
  position: relative;
  z-index: 1;
}

.stats-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
  gap: 3rem;
  max-width: 1000px;
  margin: 0 auto;
  position: relative;
  z-index: 1;
}

.stat-item {
  padding: 2rem 1.5rem;
  border-radius: 12px;
  background: rgba(255, 255, 255, 0.03);
  border: 1px solid rgba(255, 255, 255, 0.1);
  backdrop-filter: blur(10px);
  transition: all 0.3s ease;
}

.stat-item:hover {
  background: rgba(255, 255, 255, 0.05);
  border-color: var(--color-sage);
  transform: translateY(-4px);
}

.stat-number {
  font-family: var(--font-display);
  font-size: 3.5rem;
  font-weight: 600;
  display: block;
  margin-bottom: 0.5rem;
  color: var(--color-gold-light);
  line-height: 1;
}

.stat-label {
  font-size: 1rem;
  opacity: 0.9;
  font-weight: 400;
}

/* Responsive Design */
@media (max-width: 768px) {
  .projects-hero {
    padding: 5rem 1.5rem 4rem;
  }
  
  .hero-title {
    font-size: 3rem;
  }
  
  .hero-subtitle {
    font-size: 1.1rem;
  }
  
  .projects-grid {
    padding: 0 1.5rem;
  }
  
  .project-image-wrapper {
    height: 220px;
  }
  
  .filter-section {
    padding: 0 1.5rem;
    justify-content: flex-start;
  }
  
  .projects-stats {
    margin: 0 1.5rem 4rem;
    padding: 4rem 1.5rem;
  }
  
  .projects-stats h2 {
    font-size: 2.25rem;
  }
  
  .stats-grid {
    gap: 2rem;
  }
}

/* Accessibility */
.project-link:focus,
.filter-btn:focus {
  outline: 2px solid var(--color-sage);
  outline-offset: 2px;
}

/* Smooth scrolling */
html {
  scroll-behavior: smooth;
}
</style>

<!-- Hero Section -->
<div class="projects-hero">
  <div class="hero-content">
    <div class="hero-label">Portfolio</div>
    <h1 class="hero-title">Selected Projects</h1>
    <p class="hero-subtitle">From climate AI research to production ML systems for education, healthcare, and environmental monitoring. Building technology that solves real-world problems and creates meaningful impact.</p>
  </div>
</div>

<!-- Filter Section -->
<div class="filter-section">
  <button class="filter-btn active" onclick="filterProjects('all')">All Projects</button>
  <button class="filter-btn" onclick="filterProjects('ai-research')">AI Research</button>
  <button class="filter-btn" onclick="filterProjects('web-apps')">Web Applications</button>
  <button class="filter-btn" onclick="filterProjects('climate')">Climate Tech</button>
  <button class="filter-btn" onclick="filterProjects('education')">Education</button>
</div>

<!-- Projects Grid -->
<div class="projects-grid">
  
  <!-- Quantathon Judging App -->
  <div class="project-card" data-category="web-apps education">
    <div class="project-image-wrapper">
      <img src="https://github.com/ChantelleAA/ChantelleAA/blob/main/judging_demo.gif?raw=true" alt="Quantathon Judging App" class="project-image">
      <span class="project-category-badge">Web App</span>
    </div>
    <div class="project-content">
      <h3 class="project-title">
        <span class="emoji">🧑🏾‍⚖️</span>
        Quantathon Judging App
      </h3>
      <p class="project-description">
        A Django-based hackathon judging platform used in the <strong>AIMS Quantathon 2024</strong> with 50+ participants. Streamlined the entire judging process with real-time analytics and secure voting.
      </p>
      <ul class="project-features">
        <li>Real-time leaderboard & analytics dashboard</li>
        <li>Criteria filtered by judge expertise</li>
        <li>One-time secure voting links</li>
        <li>Admin dashboard for live event management</li>
      </ul>
      <div class="project-tech">
        <span class="tech-badge">Django</span>
        <span class="tech-badge">PostgreSQL</span>
        <span class="tech-badge">HTMX</span>
        <span class="tech-badge">Railway</span>
      </div>
      <div class="project-links">
        <a href="https://github.com/ChantelleAA/judging_criteria" class="project-link" target="_blank">
          🔗 GitHub
        </a>
        <a href="https://www.linkedin.com/posts/african-institute-for-mathematical-sciences-ghana_aimsqtedu25-quantumforgood-quantathonwinners-activity-7353129321454100482-uauo" class="project-link secondary" target="_blank">
          📰 Coverage
        </a>
      </div>
    </div>
  </div>

  <!-- TLR Helper -->
  <div class="project-card" data-category="web-apps education">
    <div class="project-image-wrapper">
      <img src="https://github.com/ChantelleAA/ChantelleAA/blob/main/tlr_helper_1.gif?raw=true" alt="TLR Helper" class="project-image">
      <span class="project-category-badge">Education</span>
    </div>
    <div class="project-content">
      <h3 class="project-title">
        <span class="emoji">📘</span>
        TLR Helper
      </h3>
      <p class="project-description">
        Teaching & Learning Resource Assistant supporting Ghana's <strong>Standards-Based Curriculum</strong>, used in TEDD Ghana teacher workshops.
      </p>
      <ul class="project-features">
        <li>Smart curriculum filtering (Class → Strand → Indicator)</li>
        <li>Offline PDFs for limited-internet schools</li>
        <li>Special needs & learning styles support</li>
        <li>Teacher resource library</li>
      </ul>
      <div class="project-tech">
        <span class="tech-badge">Django</span>
        <span class="tech-badge">HTMX</span>
        <span class="tech-badge">PostgreSQL</span>
        <span class="tech-badge">Bootstrap5</span>
      </div>
      <div class="project-links">
        <a href="https://github.com/ChantelleAA/tlr_app" class="project-link" target="_blank">
          🔗 GitHub
        </a>
      </div>
    </div>
  </div>

  <!-- Brain Tumor Segmentation -->
  <div class="project-card" data-category="ai-research">
    <div class="project-image-wrapper">
      <img src="https://github.com/ChantelleAA/ChantelleAA/blob/main/bts_img.png?raw=true" alt="Brain Tumor Segmentation" class="project-image">
      <span class="project-category-badge">AI Research</span>
    </div>
    <div class="project-content">
      <h3 class="project-title">
        <span class="emoji">🧠</span>
        Brain Tumor Segmentation
      </h3>
      <p class="project-description">
        Developed <strong>ensemble models</strong> for brain tumor segmentation on Sub-Saharan MRI data. Presented at <strong>MICCAI 2023</strong> with scholarship award.
      </p>
      <ul class="project-features">
        <li>MICCAI 2023 Scholarship recipient</li>
        <li>Novel Staple Assembling & Mednex methods</li>
        <li>Resource-limited healthcare focus</li>
        <li>Clinical application ready</li>
      </ul>
      <div class="project-tech">
        <span class="tech-badge">PyTorch</span>
        <span class="tech-badge">MONAI</span>
        <span class="tech-badge">NumPy</span>
        <span class="tech-badge">Medical Imaging</span>
      </div>
      <div class="project-links">
        <a href="https://arxiv.org/abs/2508.10905" class="project-link" target="_blank">
          📄 Paper
        </a>
        <a href="https://drive.google.com/file/d/1Mhlt9DPoW-HOK1Ky5_jtWJBCNLwpWW6M/view?usp=sharing" class="project-link secondary" target="_blank">
          📜 Certificate
        </a>
      </div>
    </div>
  </div>

  <!-- NileEdge AI Assistant -->
  <div class="project-card" data-category="ai-research web-apps">
    <div class="project-image-wrapper">
      <img src="https://github.com/ChantelleAA/ChantelleAA/blob/main/nileedgechatbot.gif?raw=true" alt="NileEdge AI" class="project-image">
      <span class="project-category-badge">AI Assistant</span>
    </div>
    <div class="project-content">
      <h3 class="project-title">
        <span class="emoji">🤖</span>
        NileEdge AI Assistant
      </h3>
      <p class="project-description">
        Context-aware chatbot with <strong>semantic FAQ matching + Whisper transcription</strong>. Privacy-first design with entirely local inference.
      </p>
      <ul class="project-features">
        <li>Hybrid retrieval + LLM inference</li>
        <li>Runs entirely locally (privacy-first)</li>
        <li>Custom UI with FAQ expansion</li>
        <li>Voice input via Whisper</li>
      </ul>
      <div class="project-tech">
        <span class="tech-badge">Python</span>
        <span class="tech-badge">Flask</span>
        <span class="tech-badge">ChromaDB</span>
        <span class="tech-badge">Whisper</span>
      </div>
      <div class="project-links">
        <a href="https://github.com/ChantelleAA/response_aigent" class="project-link" target="_blank">
          🔗 GitHub
        </a>
      </div>
    </div>
  </div>

  <!-- Oware RL -->
  <div class="project-card" data-category="ai-research">
    <div class="project-image-wrapper">
      <img src="https://github.com/ChantelleAA/ChantelleAA/blob/main/oware_demo1.gif?raw=true" alt="Oware RL" class="project-image">
      <span class="project-category-badge">Reinforcement Learning</span>
    </div>
    <div class="project-content">
      <h3 class="project-title">
        <span class="emoji">🎮</span>
        Oware Reinforcement Learning
      </h3>
      <p class="project-description">
        Full Python environment for traditional <strong>Oware</strong> game with multiple trained RL agents using state-of-the-art algorithms.
      </p>
      <ul class="project-features">
        <li>DQN, DDQN, A3C, AlphaZero implementations</li>
        <li>Human-vs-agent & agent-vs-agent modes</li>
        <li>Reward tracking & gameplay visualization</li>
        <li>Complete thesis on game theory & RL</li>
      </ul>
      <div class="project-tech">
        <span class="tech-badge">Python</span>
        <span class="tech-badge">TensorFlow</span>
        <span class="tech-badge">Stable-Baselines</span>
        <span class="tech-badge">Game Theory</span>
      </div>
      <div class="project-links">
        <a href="https://github.com/ChantelleAA/Reinforcement_Learning_Oware" class="project-link" target="_blank">
          🔗 GitHub
        </a>
        <a href="https://lutpub.lut.fi/bitstream/handle/10024/167861/mastersthesis_Amoako-Atta_Chantelle.pdf?sequence=1&isAllowed=y" class="project-link secondary" target="_blank">
          📄 Thesis
        </a>
      </div>
    </div>
  </div>

  <!-- GeoSeg Biodiversity -->
  <div class="project-card" data-category="ai-research climate">
    <div class="project-image-wrapper">
      <img src="https://github.com/ChantelleAA/ChantelleAA/blob/main/biodiversity.gif?raw=true" alt="GeoSeg" class="project-image">
      <span class="project-category-badge">Climate AI</span>
    </div>
    <div class="project-content">
      <h3 class="project-title">
        <span class="emoji">🌍</span>
        GeoSeg Biodiversity Segmentation
      </h3>
      <p class="project-description">
        Led geospatial AI for <strong>ODOS Tech</strong>, building biodiversity segmentation using Sentinel/OpenEarthMap satellite imagery.
      </p>
      <ul class="project-features">
        <li>Improved mIoU from 68–72% → 87–90%</li>
        <li>Knowledge Distillation framework</li>
        <li>Full training & evaluation pipeline</li>
        <li>Reproducible land-cover classification</li>
      </ul>
      <div class="project-tech">
        <span class="tech-badge">PyTorch</span>
        <span class="tech-badge">UNetFormer</span>
        <span class="tech-badge">GeoPandas</span>
        <span class="tech-badge">Rasterio</span>
        <span class="tech-badge">GDAL</span>
      </div>
      <div class="project-links">
        <a href="https://github.com/ChantelleAA/geoseg" class="project-link" target="_blank">
          🔗 Analysis
        </a>
        <a href="https://github.com/ChantelleAA/geseg_GAN" class="project-link secondary" target="_blank">
          🔗 Image Gen
        </a>
      </div>
    </div>
  </div>

  <!-- RTE Energy Research -->
  <div class="project-card" data-category="climate">
    <div class="project-image-wrapper">
      <img src="https://github.com/ChantelleAA/ChantelleAA/blob/main/air-quality-app.gif?raw=true" alt="RTE Energy" class="project-image">
      <span class="project-category-badge">Climate</span>
    </div>
    <div class="project-content">
      <h3 class="project-title">
        <span class="emoji">🔋</span>
        RTE Energy Research Dashboard
      </h3>
      <p class="project-description">
        Multi-city pollution dashboards for RTE Investigates research on renewable energy costs with satellite & ground sensor fusion.
      </p>
      <ul class="project-features">
        <li>Air-quality analytics for multiple cities</li>
        <li>Satellite + ground sensor data fusion</li>
        <li>Trend analysis & geo-scatter maps</li>
        <li>Decarb-AI research insights</li>
      </ul>
      <div class="project-tech">
        <span class="tech-badge">Streamlit</span>
        <span class="tech-badge">GeoPandas</span>
        <span class="tech-badge">Plotly</span>
        <span class="tech-badge">Pandas</span>
      </div>
      <div class="project-links">
        <a href="https://github.com/ChantelleAA/urumqi_analysis" class="project-link" target="_blank">
          🔗 Analysis
        </a>
        <a href="https://github.com/ChantelleAA/pollution_viz" class="project-link secondary" target="_blank">
          🔗 Dashboard
        </a>
      </div>
    </div>
  </div>

  <!-- OCR Research -->
  <div class="project-card" data-category="ai-research">
    <div class="project-image-wrapper">
      <div style="height: 280px; background: linear-gradient(135deg, #F5F3EF 0%, #E8E5DF 100%); display: flex; align-items: center; justify-content: center;">
        <span style="font-size: 5rem;">📄</span>
      </div>
      <span class="project-category-badge">Research</span>
    </div>
    <div class="project-content">
      <h3 class="project-title">
        <span class="emoji">📄</span>
        OCR Research & Evaluation
      </h3>
      <p class="project-description">
        Comprehensive research evaluating state-of-the-art OCR tools for document processing with focus on low-resource languages.
      </p>
      <ul class="project-features">
        <li>Benchmarking multiple OCR engines</li>
        <li>Performance metrics comparison</li>
        <li>Preprocessing pipeline optimization</li>
        <li>Low-resource language support</li>
      </ul>
      <div class="project-tech">
        <span class="tech-badge">Python</span>
        <span class="tech-badge">Tesseract</span>
        <span class="tech-badge">EasyOCR</span>
        <span class="tech-badge">PaddleOCR</span>
        <span class="tech-badge">OpenCV</span>
      </div>
    </div>
  </div>

  <!-- GeoAI Workshop -->
  <div class="project-card" data-category="education climate">
    <div class="project-image-wrapper">
      <img src="https://github.com/ChantelleAA/ChantelleAA/blob/main/geoai workshop.gif?raw=true" alt="GeoAI Workshop" class="project-image">
      <span class="project-category-badge">Education</span>
    </div>
    <div class="project-content">
      <h3 class="project-title">
        <span class="emoji">🌍</span>
        GeoAI Workshop Materials
      </h3>
      <p class="project-description">
        Workshop materials for geospatial AI and environmental monitoring, delivered at GAIN conference with hands-on tutorials.
      </p>
      <ul class="project-features">
        <li>Satellite imagery processing tutorials</li>
        <li>Land cover ML classification</li>
        <li>Environmental data analysis</li>
        <li>Jupyter notebooks for remote sensing</li>
      </ul>
      <div class="project-tech">
        <span class="tech-badge">Python</span>
        <span class="tech-badge">Jupyter</span>
        <span class="tech-badge">GeoPandas</span>
        <span class="tech-badge">Rasterio</span>
        <span class="tech-badge">QGIS</span>
      </div>
      <div class="project-links">
        <a href="https://github.com/ChantelleAA/gain_geoai_workshop" class="project-link" target="_blank">
          🔗 GitHub
        </a>
      </div>
    </div>
  </div>

</div>

<!-- Stats Section -->
<div class="projects-stats">
  <h2>Impact & Recognition</h2>
  <div class="stats-grid">
    <div class="stat-item">
      <span class="stat-number">9</span>
      <span class="stat-label">Major Projects</span>
    </div>
    <div class="stat-item">
      <span class="stat-number">5</span>
      <span class="stat-label">Publications</span>
    </div>
    <div class="stat-item">
      <span class="stat-number">200+</span>
      <span class="stat-label">Students Taught</span>
    </div>
    <div class="stat-item">
      <span class="stat-number">3</span>
      <span class="stat-label">Hackathon Wins</span>
    </div>
  </div>
</div>

<script>
function filterProjects(category) {
  const cards = document.querySelectorAll('.project-card');
  const buttons = document.querySelectorAll('.filter-btn');
  
  // Update active button
  buttons.forEach(btn => btn.classList.remove('active'));
  event.target.classList.add('active');
  
  // Filter cards
  cards.forEach(card => {
    if (category === 'all') {
      card.style.display = 'block';
    } else {
      const categories = card.getAttribute('data-category');
      if (categories && categories.includes(category)) {
        card.style.display = 'block';
      } else {
        card.style.display = 'none';
      }
    }
  });
}
</script>

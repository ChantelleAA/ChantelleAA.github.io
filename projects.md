---
layout: default
title: Projects
permalink: /projects/
---

<style>
/* Hero Section */
.projects-hero {
  background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
  color: white;
  padding: 6rem 2rem 5rem;
  margin: -2rem -2rem 4rem -2rem;
  text-align: center;
  position: relative;
  overflow: hidden;
}

.projects-hero::before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background: url('data:image/svg+xml,<svg width="100" height="100" xmlns="http://www.w3.org/2000/svg"><defs><pattern id="grid" width="100" height="100" patternUnits="userSpaceOnUse"><path d="M 100 0 L 0 0 0 100" fill="none" stroke="rgba(255,255,255,0.05)" stroke-width="1"/></pattern></defs><rect width="100%" height="100%" fill="url(%23grid)"/></svg>');
  animation: moveGrid 20s linear infinite;
}

@keyframes moveGrid {
  0% { transform: translate(0, 0); }
  100% { transform: translate(100px, 100px); }
}

.hero-content {
  max-width: 900px;
  margin: 0 auto;
  position: relative;
  z-index: 1;
}

.hero-title {
  font-size: 3.5rem;
  font-weight: 800;
  margin-bottom: 1.5rem;
  letter-spacing: -1px;
  text-shadow: 0 2px 20px rgba(0,0,0,0.2);
}

.hero-subtitle {
  font-size: 1.3rem;
  font-weight: 300;
  line-height: 1.8;
  opacity: 0.95;
  max-width: 700px;
  margin: 0 auto;
}

/* Filter Section */
.filter-section {
  background: white;
  padding: 2rem;
  border-radius: 16px;
  box-shadow: 0 4px 20px rgba(0,0,0,0.08);
  margin-bottom: 3rem;
  display: flex;
  gap: 1rem;
  flex-wrap: wrap;
  align-items: center;
  justify-content: center;
}

.filter-btn {
  padding: 0.75rem 1.5rem;
  border: 2px solid #e1e8ed;
  background: white;
  color: #555;
  border-radius: 30px;
  font-weight: 600;
  cursor: pointer;
  transition: all 0.3s ease;
  font-size: 0.95rem;
}

.filter-btn:hover {
  border-color: #FBBF24;
  color: #F59E0B;
  transform: translateY(-2px);
}

.filter-btn.active {
  background: linear-gradient(135deg, #FBBF24, #FCD34D);
  color: #1F2937;
  border-color: #FBBF24;
  box-shadow: 0 4px 15px rgba(251, 191, 36, 0.3);
}

/* Projects Grid */
.projects-grid {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(450px, 1fr));
  gap: 3rem;
  margin-bottom: 4rem;
}

@media (max-width: 768px) {
  .projects-grid {
    grid-template-columns: 1fr;
  }
}

/* Project Card */
.project-card {
  background: white;
  border-radius: 20px;
  overflow: hidden;
  box-shadow: 0 8px 30px rgba(0,0,0,0.08);
  transition: all 0.4s cubic-bezier(0.175, 0.885, 0.32, 1.275);
  position: relative;
  border: 1px solid rgba(0,0,0,0.05);
}

.project-card:hover {
  transform: translateY(-12px);
  box-shadow: 0 20px 50px rgba(102, 126, 234, 0.2);
  border-color: #FBBF24;
}

.project-image-wrapper {
  position: relative;
  width: 100%;
  height: 280px;
  overflow: hidden;
  background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
}

.project-image {
  width: 100%;
  height: 100%;
  object-fit: cover;
  transition: transform 0.6s ease;
}

.project-card:hover .project-image {
  transform: scale(1.08);
}

.project-category-badge {
  position: absolute;
  top: 1rem;
  right: 1rem;
  background: rgba(255, 255, 255, 0.95);
  color: #667eea;
  padding: 0.5rem 1rem;
  border-radius: 20px;
  font-size: 0.85rem;
  font-weight: 700;
  text-transform: uppercase;
  letter-spacing: 0.5px;
  box-shadow: 0 4px 15px rgba(0,0,0,0.15);
}

.project-content {
  padding: 2rem;
}

.project-title {
  font-size: 1.5rem;
  font-weight: 700;
  color: #2c3e50;
  margin-bottom: 1rem;
  line-height: 1.3;
  display: flex;
  align-items: center;
  gap: 0.5rem;
}

.project-title .emoji {
  font-size: 1.8rem;
}

.project-description {
  font-size: 1rem;
  line-height: 1.7;
  color: #666;
  margin-bottom: 1.5rem;
}

.project-features {
  list-style: none;
  padding: 0;
  margin: 1.5rem 0;
}

.project-features li {
  padding: 0.5rem 0;
  padding-left: 1.8rem;
  position: relative;
  font-size: 0.95rem;
  color: #555;
  line-height: 1.6;
}

.project-features li:before {
  content: "✓";
  position: absolute;
  left: 0;
  color: #FBBF24;
  font-weight: bold;
  font-size: 1.2rem;
}

.project-tech {
  display: flex;
  flex-wrap: wrap;
  gap: 0.5rem;
  margin: 1.5rem 0;
  padding-top: 1.5rem;
  border-top: 1px solid #f0f2f5;
}

.tech-badge {
  padding: 0.4rem 0.9rem;
  background: linear-gradient(135deg, #f8fafc, #f1f5f9);
  color: #667eea;
  border-radius: 20px;
  font-size: 0.8rem;
  font-weight: 600;
  border: 1px solid #e2e8f0;
  transition: all 0.3s ease;
}

.tech-badge:hover {
  background: linear-gradient(135deg, #667eea, #764ba2);
  color: white;
  transform: translateY(-2px);
}

.project-links {
  display: flex;
  gap: 0.75rem;
  flex-wrap: wrap;
  margin-top: 1.5rem;
}

.project-link {
  display: inline-flex;
  align-items: center;
  gap: 0.5rem;
  padding: 0.75rem 1.25rem;
  background: linear-gradient(135deg, #FBBF24, #FCD34D);
  color: #1F2937;
  text-decoration: none;
  border-radius: 12px;
  font-weight: 600;
  font-size: 0.9rem;
  transition: all 0.3s ease;
  box-shadow: 0 4px 12px rgba(251, 191, 36, 0.2);
}

.project-link:hover {
  transform: translateY(-3px);
  box-shadow: 0 8px 20px rgba(251, 191, 36, 0.4);
  background: linear-gradient(135deg, #F59E0B, #FBBF24);
}

.project-link.secondary {
  background: white;
  color: #667eea;
  border: 2px solid #667eea;
  box-shadow: none;
}

.project-link.secondary:hover {
  background: #667eea;
  color: white;
}

/* Stats Section */
.projects-stats {
  background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
  padding: 4rem 2rem;
  border-radius: 20px;
  margin: 4rem 0;
  text-align: center;
  color: white;
}

.projects-stats h2 {
  font-size: 2.5rem;
  font-weight: 800;
  margin-bottom: 3rem;
}

.stats-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
  gap: 2rem;
  max-width: 900px;
  margin: 0 auto;
}

.stat-item {
  background: rgba(255, 255, 255, 0.1);
  padding: 2rem;
  border-radius: 16px;
  backdrop-filter: blur(10px);
  border: 1px solid rgba(255, 255, 255, 0.2);
}

.stat-number {
  font-size: 3rem;
  font-weight: 800;
  display: block;
  margin-bottom: 0.5rem;
  color: #FBBF24;
}

.stat-label {
  font-size: 1rem;
  opacity: 0.95;
}

/* Responsive Design */
@media (max-width: 768px) {
  .hero-title {
    font-size: 2.5rem;
  }
  
  .hero-subtitle {
    font-size: 1.1rem;
  }
  
  .projects-grid {
    gap: 2rem;
  }
  
  .project-image-wrapper {
    height: 220px;
  }
  
  .filter-section {
    justify-content: flex-start;
  }
}

/* Loading Animation */
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

.project-card {
  animation: fadeInUp 0.6s ease-out backwards;
}

.project-card:nth-child(1) { animation-delay: 0.1s; }
.project-card:nth-child(2) { animation-delay: 0.2s; }
.project-card:nth-child(3) { animation-delay: 0.3s; }
.project-card:nth-child(4) { animation-delay: 0.4s; }
.project-card:nth-child(5) { animation-delay: 0.5s; }
.project-card:nth-child(6) { animation-delay: 0.6s; }
.project-card:nth-child(7) { animation-delay: 0.7s; }
.project-card:nth-child(8) { animation-delay: 0.8s; }
.project-card:nth-child(9) { animation-delay: 0.9s; }
</style>

<!-- Hero Section -->
<div class="projects-hero">
  <div class="hero-content">
    <h1 class="hero-title">My Projects Portfolio</h1>
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
      <div style="height: 280px; background: linear-gradient(135deg, #667eea 0%, #764ba2 100%); display: flex; align-items: center; justify-content: center;">
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

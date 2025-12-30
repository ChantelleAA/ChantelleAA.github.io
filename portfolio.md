---
layout: page
title: Portfolio
permalink: /portfolio/
---

<div class="portfolio-page">

<!-- Hero Section -->
<section class="hero section-sm">
  <div class="container-lg">
    <div style="display: flex; align-items: center; gap: 3rem; flex-wrap: wrap-reverse;">
      <div style="flex: 1; min-width: 300px;">
        <h1 style="font-size: clamp(2.5rem, 5vw, 3.5rem); font-weight: 800; margin-bottom: 1rem; line-height: 1.2;">
          <span class="text-gradient">AI Researcher & ML Engineer</span>
        </h1>
        <p style="font-size: 1.25rem; color: var(--text-secondary, #475569); margin-bottom: 2rem; line-height: 1.6;">
          PhD researcher specializing in AI for climate, applying machine learning to environmental systems and building practical solutions for real-world challenges.
        </p>
        <div style="display: flex; gap: 1rem; margin-bottom: 1.5rem; flex-wrap: wrap;">
          <a href="#projects" class="btn btn-primary btn-lg">
            <i class="fa-solid fa-folder-open"></i> View Projects
          </a>
          <a href="/Resume/" class="btn btn-outline btn-lg">
            <i class="fa-solid fa-download"></i> Download Resume
          </a>
        </div>
        <div style="display: flex; gap: 1rem;">
          <a href="https://github.com/ChantelleAA" class="btn-icon btn-outline" target="_blank" rel="noopener" aria-label="GitHub">
            <i class="fa-brands fa-github"></i>
          </a>
          <a href="https://linkedin.com/in/chantelleaa" class="btn-icon btn-outline" target="_blank" rel="noopener" aria-label="LinkedIn">
            <i class="fa-brands fa-linkedin-in"></i>
          </a>
          <a href="mailto:chantelatta@gmail.com" class="btn-icon btn-outline" aria-label="Email">
            <i class="fa-solid fa-envelope"></i>
          </a>
        </div>
      </div>
      <div style="flex-shrink: 0;">
        <img src="/Chantelle.jpeg" alt="Chantelle Amoako-Atta" style="width: 280px; height: 280px; border-radius: 50%; object-fit: cover; border: 6px solid rgba(255, 255, 255, 0.9); box-shadow: 0 25px 50px rgba(37, 99, 235, 0.3);">
      </div>
    </div>
  </div>
</section>

<!-- Stats Dashboard -->
{% include stats-section.html 
  stat1_number="12+"
  stat1_label="Projects Completed"
  stat1_icon="fa-solid fa-code-branch"
  stat2_number="500+"
  stat2_label="Students Taught"
  stat2_icon="fa-solid fa-graduation-cap"
  stat3_number="3"
  stat3_label="Publications"
  stat3_icon="fa-solid fa-file-lines"
  stat4_number="4+"
  stat4_label="Years Experience"
  stat4_icon="fa-solid fa-clock"
%}

<!-- Current Research Focus -->
<section class="section" style="background-color: var(--bg-secondary, #f8fafc);">
  <div class="container-lg">
    <div style="text-align: center; margin-bottom: 3rem;">
      <h2 style="font-size: 2.5rem; font-weight: 800; margin-bottom: 1rem;">Current Research Focus</h2>
      <p style="font-size: 1.25rem; color: var(--text-secondary, #475569); max-width: 700px; margin: 0 auto;">
        PhD Researcher in Decarb-AI at University College Dublin, applying AI to climate, energy, and environmental systems
      </p>
    </div>
    
    <div class="grid grid-cols-2" style="gap: 1.5rem;">
      <div class="card" style="padding: 1.5rem;">
        <i class="fa-solid fa-satellite" style="font-size: 2.5rem; color: var(--primary-color, #2563eb); margin-bottom: 1rem; display: block;"></i>
        <h3 style="font-size: 1.25rem; font-weight: 700; margin-bottom: 0.5rem;">Remote Sensing & Geospatial AI</h3>
        <p style="color: var(--text-secondary, #475569);">Sentinel, Copernicus, OpenEarthMap analysis</p>
      </div>
      
      <div class="card" style="padding: 1.5rem;">
        <i class="fa-solid fa-earth-americas" style="font-size: 2.5rem; color: var(--primary-color, #2563eb); margin-bottom: 1rem; display: block;"></i>
        <h3 style="font-size: 1.25rem; font-weight: 700; margin-bottom: 0.5rem;">Land-cover Segmentation</h3>
        <p style="color: var(--text-secondary, #475569);">UNetFormer, FT-UNetFormer & DCSwin architectures</p>
      </div>
      
      <div class="card" style="padding: 1.5rem;">
        <i class="fa-solid fa-network-wired" style="font-size: 2.5rem; color: var(--primary-color, #2563eb); margin-bottom: 1rem; display: block;"></i>
        <h3 style="font-size: 1.25rem; font-weight: 700; margin-bottom: 0.5rem;">Knowledge Distillation</h3>
        <p style="color: var(--text-secondary, #475569);">Teacher-student architectures for efficient segmentation</p>
      </div>
      
      <div class="card" style="padding: 1.5rem;">
        <i class="fa-solid fa-smog" style="font-size: 2.5rem; color: var(--primary-color, #2563eb); margin-bottom: 1rem; display: block;"></i>
        <h3 style="font-size: 1.25rem; font-weight: 700; margin-bottom: 0.5rem;">Air Quality Analysis</h3>
        <p style="color: var(--text-secondary, #475569);">Pollution mapping using multi-city datasets</p>
      </div>
      
      <div class="card" style="padding: 1.5rem;">
        <i class="fa-solid fa-bolt" style="font-size: 2.5rem; color: var(--primary-color, #2563eb); margin-bottom: 1rem; display: block;"></i>
        <h3 style="font-size: 1.25rem; font-weight: 700; margin-bottom: 0.5rem;">Energy Decarbonization</h3>
        <p style="color: var(--text-secondary, #475569);">Analytics for energy system optimization</p>
      </div>
      
      <div class="card" style="padding: 1.5rem;">
        <i class="fa-solid fa-brain" style="font-size: 2.5rem; color: var(--primary-color, #2563eb); margin-bottom: 1rem; display: block;"></i>
        <h3 style="font-size: 1.25rem; font-weight: 700; margin-bottom: 0.5rem;">Hybrid AI Systems</h3>
        <p style="color: var(--text-secondary, #475569);">NLP + Computer Vision for sustainability</p>
      </div>
      
      <div class="card" style="padding: 1.5rem;">
        <i class="fa-solid fa-chart-line" style="font-size: 2.5rem; color: var(--primary-color, #2563eb); margin-bottom: 1rem; display: block;"></i>
        <h3 style="font-size: 1.25rem; font-weight: 700; margin-bottom: 0.5rem;">Data Fusion</h3>
        <p style="color: var(--text-secondary, #475569);">Satellite + ground-sensor climate-risk assessment</p>
      </div>
      
      <div class="card" style="padding: 1.5rem;">
        <i class="fa-solid fa-file-text" style="font-size: 2.5rem; color: var(--primary-color, #2563eb); margin-bottom: 1rem; display: block;"></i>
        <h3 style="font-size: 1.25rem; font-weight: 700; margin-bottom: 0.5rem;">OCR & Document AI</h3>
        <p style="color: var(--text-secondary, #475569);">Benchmarking for low-resource languages</p>
      </div>
    </div>
  </div>
</section>

<!-- Featured Projects -->
<section id="projects" class="section">
  <div class="container-lg">
    <div style="text-center mb-8">
      <h2 style="font-size: 3rem; font-weight: 800; margin-bottom: 1rem;">Featured Projects</h2>
      <p style="font-size: 1.25rem; color: var(--text-secondary, #475569);">Explore my work in AI research, web development, and education</p>
    </div>
    
    {% include filter-bar.html 
      categories="Research, Web Apps, ML/AI, Education"
      placeholder="Search projects by name or technology..."
      filter_type="projects"
    %}
    
    <div class="grid grid-cols-3" data-filter-container="projects" style="margin-top: 2rem;">
      
      <!-- Project 1: Quantathon Judging App -->
      <div data-filterable="projects" data-category="web-apps" data-title="Quantathon Judging App" data-tags="Django PostgreSQL HTMX" data-date="2024">
        <div class="project-card">
          <div class="project-image">
            <img src="/assets/images/projects/judging_demo.gif" alt="Quantathon Judging App demo" loading="lazy">
            <div class="project-category">
              <span class="pill pill-sm pill-primary">Web App</span>
            </div>
          </div>
          
          <div class="project-content">
            <h3 class="project-title">Quantathon Judging App</h3>
            
            <p class="project-description">A Django-based hackathon judging platform used in the AIMS Quantathon 2024 with 50+ participants. Features real-time leaderboard, analytics, criteria filtered by judge expertise, one-time secure voting links, and admin dashboard for managing live events.</p>
            
            <div class="project-tech-stack">
              <span class="pill pill-sm pill-secondary">Django</span>
              <span class="pill pill-sm pill-secondary">PostgreSQL</span>
              <span class="pill pill-sm pill-secondary">HTMX</span>
              <span class="pill pill-sm pill-secondary">Railway</span>
            </div>
            
            <div class="project-metrics">
              <div class="metric">
                <i class="fa-solid fa-users"></i>
                <span>50+ participants</span>
              </div>
            </div>
            
            <div class="project-footer">
              <a href="https://github.com/ChantelleAA/judging_criteria" class="btn btn-primary btn-sm" target="_blank" rel="noopener">
                <i class="fa-brands fa-github"></i> GitHub
              </a>
              <a href="https://www.linkedin.com/posts/african-institute-for-mathematical-sciences-ghana_aimsqtedu25-quantumforgood-quantathonwinners-activity-7353129321454100482-uauo" class="btn btn-outline btn-sm" target="_blank" rel="noopener">
                <i class="fa-solid fa-newspaper"></i> Press
              </a>
            </div>
          </div>
        </div>
      </div>
      
      <!-- Project 2: TLR Helper -->
      <div data-filterable="projects" data-category="education" data-title="TLR Helper Teaching Resource Assistant" data-tags="Django HTMX PostgreSQL Bootstrap" data-date="2024">
        <div class="project-card">
          <div class="project-image">
            <img src="/assets/images/projects/tlr_helper_1.gif" alt="TLR Helper demo" loading="lazy">
            <div class="project-category">
              <span class="pill pill-sm pill-accent">Education</span>
            </div>
          </div>
          
          <div class="project-content">
            <h3 class="project-title">TLR Helper – Teaching Resource Assistant</h3>
            
            <p class="project-description">A web app supporting Ghana's Standards-Based Curriculum, used in TEDD Ghana teacher workshops. Smart curriculum filtering, offline PDFs for schools with limited internet, and built-in support for special needs and learning styles.</p>
            
            <div class="project-tech-stack">
              <span class="pill pill-sm pill-secondary">Django</span>
              <span class="pill pill-sm pill-secondary">HTMX</span>
              <span class="pill pill-sm pill-secondary">PostgreSQL</span>
              <span class="pill pill-sm pill-secondary">Bootstrap5</span>
            </div>
            
            <div class="project-footer">
              <a href="https://github.com/ChantelleAA/tlr_app" class="btn btn-primary btn-sm" target="_blank" rel="noopener">
                <i class="fa-brands fa-github"></i> GitHub
              </a>
            </div>
          </div>
        </div>
      </div>
      
      <!-- Project 3: Brain Tumor Segmentation -->
      <div data-filterable="projects" data-category="research" data-title="Brain Tumor Segmentation MICCAI" data-tags="PyTorch MONAI Medical-Imaging" data-date="2023">
        <div class="project-card">
          <div class="project-image">
            <img src="/assets/images/projects/bts_img.png" alt="Brain tumor segmentation" loading="lazy">
            <div class="project-category">
              <span class="pill pill-sm pill-success">Research</span>
            </div>
          </div>
          
          <div class="project-content">
            <h3 class="project-title">Brain Tumor Segmentation (MICCAI)</h3>
            
            <p class="project-description">Developed ensemble models to improve segmentation on Sub-Saharan MRI data. Awarded MICCAI 2023 Scholarship to present this work internationally. Proposed new methods (Staple Assembling & Mednex) for better outcomes.</p>
            
            <div class="project-tech-stack">
              <span class="pill pill-sm pill-secondary">PyTorch</span>
              <span class="pill pill-sm pill-secondary">MONAI</span>
              <span class="pill pill-sm pill-secondary">NumPy</span>
              <span class="pill pill-sm pill-secondary">Python</span>
            </div>
            
            <div class="project-footer">
              <a href="https://arxiv.org/abs/2508.10905" class="btn btn-primary btn-sm" target="_blank" rel="noopener">
                <i class="fa-solid fa-file-pdf"></i> Paper
              </a>
              <a href="https://drive.google.com/file/d/1Mhlt9DPoW-HOK1Ky5_jtWJBCNLwpWW6M/view" class="btn btn-outline btn-sm" target="_blank" rel="noopener">
                <i class="fa-solid fa-certificate"></i> Certificate
              </a>
            </div>
          </div>
        </div>
      </div>
      
      <!-- Project 4: NileEdge AI Assistant -->
      <div data-filterable="projects" data-category="ml-ai" data-title="NileEdge AI Chatbot" data-tags="Python Flask ChromaDB Whisper" data-date="2024">
        <div class="project-card">
          <div class="project-image">
            <img src="/assets/images/projects/nileedgechatbot.gif" alt="NileEdge AI Chatbot demo" loading="lazy">
            <div class="project-category">
              <span class="pill pill-sm pill-info">ML/AI</span>
            </div>
          </div>
          
          <div class="project-content">
            <h3 class="project-title">NileEdge AI Assistant</h3>
            
            <p class="project-description">A context-aware chatbot with semantic FAQ matching + Whisper transcription, built for NileEdge Innovations. Hybrid retrieval + LLM inference, privacy-first running entirely locally, custom UI with automatic FAQ expansion.</p>
            
            <div class="project-tech-stack">
              <span class="pill pill-sm pill-secondary">Python</span>
              <span class="pill pill-sm pill-secondary">Flask</span>
              <span class="pill pill-sm pill-secondary">ChromaDB</span>
              <span class="pill pill-sm pill-secondary">Whisper</span>
            </div>
            
            <div class="project-footer">
              <a href="https://github.com/ChantelleAA/response_aigent" class="btn btn-primary btn-sm" target="_blank" rel="noopener">
                <i class="fa-brands fa-github"></i> GitHub
              </a>
            </div>
          </div>
        </div>
      </div>
      
      <!-- Project 5: Oware RL -->
      <div data-filterable="projects" data-category="ml-ai" data-title="Oware Reinforcement Learning" data-tags="Python TensorFlow RL" data-date="2023">
        <div class="project-card">
          <div class="project-image">
            <img src="/assets/images/projects/oware_demo1.gif" alt="Oware RL demo" loading="lazy">
            <div class="project-category">
              <span class="pill pill-sm pill-info">ML/AI</span>
            </div>
          </div>
          
          <div class="project-content">
            <h3 class="project-title">Oware Nam-nam Reinforcement Learning</h3>
            
            <p class="project-description">Built a full Python environment for the traditional game Oware and trained multiple agents. Implemented DQN, DDQN, A3C, AlphaZero with human-vs-agent and agent-vs-agent play modes. Includes reward tracking and gameplay visualization.</p>
            
            <div class="project-tech-stack">
              <span class="pill pill-sm pill-secondary">Python</span>
              <span class="pill pill-sm pill-secondary">TensorFlow</span>
              <span class="pill pill-sm pill-secondary">Stable-Baselines</span>
            </div>
            
            <div class="project-footer">
              <a href="https://github.com/ChantelleAA/Reinforcement_Learning_Oware" class="btn btn-primary btn-sm" target="_blank" rel="noopener">
                <i class="fa-brands fa-github"></i> GitHub
              </a>
              <a href="https://lutpub.lut.fi/bitstream/handle/10024/167861/mastersthesis_Amoako-Atta_Chantelle.pdf" class="btn btn-outline btn-sm" target="_blank" rel="noopener">
                <i class="fa-solid fa-file-pdf"></i> Thesis
              </a>
            </div>
          </div>
        </div>
      </div>
      
      <!-- Project 6: GeoSeg Biodiversity -->
      <div data-filterable="projects" data-category="research" data-title="GeoSeg Biodiversity Segmentation" data-tags="PyTorch UNetFormer GeoPandas" data-date="2024">
        <div class="project-card">
          <div class="project-image">
            <img src="/assets/images/projects/biodiversity.gif" alt="GeoSeg demo" loading="lazy">
            <div class="project-category">
              <span class="pill pill-sm pill-success">Research</span>
            </div>
          </div>
          
          <div class="project-content">
            <h3 class="project-title">AI Sandbox – GeoSeg Biodiversity Segmentation</h3>
            
            <p class="project-description">Led geospatial AI work for ODOS Tech, building a biodiversity segmentation pipeline using Sentinel/OpenEarthMap. Improved mIoU from 68-72% to 87-90%. Designed Knowledge Distillation teacher-student framework.</p>
            
            <div class="project-tech-stack">
              <span class="pill pill-sm pill-secondary">PyTorch</span>
              <span class="pill pill-sm pill-secondary">UNetFormer</span>
              <span class="pill pill-sm pill-secondary">GeoPandas</span>
              <span class="pill pill-sm pill-secondary">Rasterio</span>
            </div>
            
            <div class="project-metrics">
              <div class="metric">
                <i class="fa-solid fa-chart-line"></i>
                <span>87-90% mIoU (from 68-72%)</span>
              </div>
            </div>
            
            <div class="project-footer">
              <a href="https://github.com/ChantelleAA/geoseg" class="btn btn-primary btn-sm" target="_blank" rel="noopener">
                <i class="fa-brands fa-github"></i> Analysis
              </a>
              <a href="https://github.com/ChantelleAA/geseg_GAN" class="btn btn-outline btn-sm" target="_blank" rel="noopener">
                <i class="fa-brands fa-github"></i> Image Gen
              </a>
            </div>
          </div>
        </div>
      </div>
      
      <!-- Project 7: RTE Energy Dashboard -->
      <div data-filterable="projects" data-category="research" data-title="RTE Pollution Dashboard" data-tags="Streamlit GeoPandas Plotly" data-date="2024">
        <div class="project-card">
          <div class="project-image">
            <img src="/assets/images/projects/air-quality-app.gif" alt="RTE Demo" loading="lazy">
            <div class="project-category">
              <span class="pill pill-sm pill-success">Research</span>
            </div>
          </div>
          
          <div class="project-content">
            <h3 class="project-title">RTE Energy Research – Pollution Dashboard</h3>
            
            <p class="project-description">Developed multi-city pollution dashboards as part of research for RTE Investigates story on renewable energy cost. Air-quality analytics for multiple Chinese cities with satellite bounding box extraction + ground sensor fusion.</p>
            
            <div class="project-tech-stack">
              <span class="pill pill-sm pill-secondary">Streamlit</span>
              <span class="pill pill-sm pill-secondary">GeoPandas</span>
              <span class="pill pill-sm pill-secondary">Plotly</span>
              <span class="pill pill-sm pill-secondary">Pandas</span>
            </div>
            
            <div class="project-footer">
              <a href="https://github.com/ChantelleAA/urumqi_analysis" class="btn btn-primary btn-sm" target="_blank" rel="noopener">
                <i class="fa-brands fa-github"></i> Analysis
              </a>
              <a href="https://github.com/ChantelleAA/pollution_viz" class="btn btn-outline btn-sm" target="_blank" rel="noopener">
                <i class="fa-brands fa-github"></i> Dashboard
              </a>
            </div>
          </div>
        </div>
      </div>
      
      <!-- Project 8: OCR Research -->
      <div data-filterable="projects" data-category="research" data-title="OCR Research Evaluation" data-tags="Python Tesseract EasyOCR OpenCV" data-date="2024">
        <div class="project-card">
          <div class="project-content" style="padding-top: 1.5rem;">
            <h3 class="project-title">OCR Research & Evaluation</h3>
            
            <p class="project-description">Comprehensive research project evaluating state-of-the-art OCR tools for document processing. Benchmarking multiple OCR engines (Tesseract, EasyOCR, PaddleOCR), performance metrics comparison, and preprocessing pipeline optimization for improved accuracy.</p>
            
            <div class="project-tech-stack">
              <span class="pill pill-sm pill-secondary">Python</span>
              <span class="pill pill-sm pill-secondary">Tesseract</span>
              <span class="pill pill-sm pill-secondary">EasyOCR</span>
              <span class="pill pill-sm pill-secondary">OpenCV</span>
            </div>
          </div>
        </div>
      </div>
      
      <!-- Project 9: GeoAI Workshop -->
      <div data-filterable="projects" data-category="education" data-title="GeoAI Workshop" data-tags="Python Jupyter GeoPandas QGIS" data-date="2024">
        <div class="project-card">
          <div class="project-image">
            <img src="/assets/images/projects/geoai_workshop.gif" alt="GEOAI Workshop" loading="lazy">
            <div class="project-category">
              <span class="pill pill-sm pill-accent">Education</span>
            </div>
          </div>
          
          <div class="project-content">
            <h3 class="project-title">GeoAI Workshop – Satellite Data Analysis</h3>
            
            <p class="project-description">Workshop materials and teaching resources for geospatial AI and environmental monitoring. Hands-on tutorials for satellite imagery processing, land cover classification using machine learning, and environmental data analysis with Python.</p>
            
            <div class="project-tech-stack">
              <span class="pill pill-sm pill-secondary">Python</span>
              <span class="pill pill-sm pill-secondary">Jupyter</span>
              <span class="pill pill-sm pill-secondary">GeoPandas</span>
              <span class="pill pill-sm pill-secondary">QGIS</span>
            </div>
            
            <div class="project-footer">
              <a href="https://github.com/ChantelleAA/gain_geoai_workshop" class="btn btn-primary btn-sm" target="_blank" rel="noopener">
                <i class="fa-brands fa-github"></i> GitHub
              </a>
            </div>
          </div>
        </div>
      </div>
      
    </div>
  </div>
</section>

<!-- Tech Stack Section -->
<section class="section" style="background-color: var(--bg-secondary, #f8fafc);">
  <div class="container-lg">
    <div style="text-center; margin-bottom: 3rem;">
      <h2 style="font-size: 3rem; font-weight: 800; margin-bottom: 1rem;">Tech Stack & Skills</h2>
      <p style="font-size: 1.25rem; color: var(--text-secondary, #475569);">Technologies and tools I work with daily</p>
    </div>
    
    <div class="grid grid-cols-2" style="gap: 2rem;">
      <!-- Programming Languages -->
      <div class="card" style="padding: 2rem;">
        <h3 style="font-size: 1.5rem; font-weight: 700; margin-bottom: 1.5rem; display: flex; align-items: center; gap: 0.5rem;">
          <i class="fa-solid fa-code" style="color: var(--primary-color, #2563eb);"></i>
          Programming Languages
        </h3>
        <div style="display: flex; flex-wrap: wrap; gap: 0.75rem;">
          <img src="https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54" alt="Python">
          <img src="https://img.shields.io/badge/R-276DC3?style=for-the-badge&logo=r&logoColor=white" alt="R">
          <img src="https://img.shields.io/badge/MATLAB-%23e37922.svg?style=for-the-badge&logo=Mathworks&logoColor=white" alt="MATLAB">
          <img src="https://img.shields.io/badge/Julia-9558B2?style=for-the-badge&logo=julia&logoColor=white" alt="Julia">
          <img src="https://img.shields.io/badge/sql-%23007ACC.svg?style=for-the-badge&logo=sqlite&logoColor=white" alt="SQL">
        </div>
      </div>
      
      <!-- Machine Learning & Deep Learning -->
      <div class="card" style="padding: 2rem;">
        <h3 style="font-size: 1.5rem; font-weight: 700; margin-bottom: 1.5rem; display: flex; align-items: center; gap: 0.5rem;">
          <i class="fa-solid fa-robot" style="color: var(--primary-color, #2563eb);"></i>
          ML & Deep Learning
        </h3>
        <div style="display: flex; flex-wrap: wrap; gap: 0.75rem;">
          <img src="https://img.shields.io/badge/TensorFlow-%23FF6F00.svg?style=for-the-badge&logo=TensorFlow&logoColor=white" alt="TensorFlow">
          <img src="https://img.shields.io/badge/Keras-D00000?style=for-the-badge&logo=keras&logoColor=white" alt="Keras">
          <img src="https://img.shields.io/badge/PyTorch-%23EE4C2C.svg?style=for-the-badge&logo=PyTorch&logoColor=white" alt="PyTorch">
          <img src="https://img.shields.io/badge/scikit--learn-%23F7931E.svg?style=for-the-badge&logo=scikit-learn&logoColor=white" alt="scikit-learn">
          <img src="https://img.shields.io/badge/XGBoost-%230079C1.svg?style=for-the-badge&logo=xgboost&logoColor=white" alt="XGBoost">
        </div>
      </div>
      
      <!-- NLP & Transformers -->
      <div class="card" style="padding: 2rem;">
        <h3 style="font-size: 1.5rem; font-weight: 700; margin-bottom: 1.5rem; display: flex; align-items: center; gap: 0.5rem;">
          <i class="fa-solid fa-language" style="color: var(--primary-color, #2563eb);"></i>
          NLP & Transformers
        </h3>
        <div style="display: flex; flex-wrap: wrap; gap: 0.75rem;">
          <img src="https://img.shields.io/badge/HuggingFace-FFD21F?style=for-the-badge&logo=huggingface&logoColor=black" alt="Hugging Face">
          <img src="https://img.shields.io/badge/SpaCy-09A3D5?style=for-the-badge&logo=spacy&logoColor=white" alt="SpaCy">
          <img src="https://img.shields.io/badge/NLTK-1A237E?style=for-the-badge&logo=nltk&logoColor=white" alt="NLTK">
        </div>
      </div>
      
      <!-- Geospatial & Computer Vision -->
      <div class="card" style="padding: 2rem;">
        <h3 style="font-size: 1.5rem; font-weight: 700; margin-bottom: 1.5rem; display: flex; align-items: center; gap: 0.5rem;">
          <i class="fa-solid fa-globe" style="color: var(--primary-color, #2563eb);"></i>
          Geospatial & CV
        </h3>
        <div style="display: flex; flex-wrap: wrap; gap: 0.75rem;">
          <img src="https://img.shields.io/badge/CUDA-76B900?style=for-the-badge&logo=nvidia&logoColor=white" alt="CUDA">
          <img src="https://img.shields.io/badge/GeoPandas-0E7C7B?style=for-the-badge&logo=python&logoColor=white" alt="GeoPandas">
          <img src="https://img.shields.io/badge/QGIS-589632?style=for-the-badge&logo=qgis&logoColor=white" alt="QGIS">
        </div>
      </div>
      
      <!-- Web Development -->
      <div class="card" style="padding: 2rem;">
        <h3 style="font-size: 1.5rem; font-weight: 700; margin-bottom: 1.5rem; display: flex; align-items: center; gap: 0.5rem;">
          <i class="fa-solid fa-window-maximize" style="color: var(--primary-color, #2563eb);"></i>
          Web Development
        </h3>
        <div style="display: flex; flex-wrap: wrap; gap: 0.75rem;">
          <img src="https://img.shields.io/badge/django-%23092E20.svg?style=for-the-badge&logo=django&logoColor=white" alt="Django">
          <img src="https://img.shields.io/badge/Flask-000000?style=for-the-badge&logo=flask&logoColor=white" alt="Flask">
          <img src="https://img.shields.io/badge/FastAPI-009688?style=for-the-badge&logo=fastapi&logoColor=white" alt="FastAPI">
          <img src="https://img.shields.io/badge/Gradio-%23404eed.svg?style=for-the-badge&logo=gradio&logoColor=white" alt="Gradio">
        </div>
      </div>
      
      <!-- Data Science & Visualization -->
      <div class="card" style="padding: 2rem;">
        <h3 style="font-size: 1.5rem; font-weight: 700; margin-bottom: 1.5rem; display: flex; align-items: center; gap: 0.5rem;">
          <i class="fa-solid fa-chart-bar" style="color: var(--primary-color, #2563eb);"></i>
          Data Science & Viz
        </h3>
        <div style="display: flex; flex-wrap: wrap; gap: 0.75rem;">
          <img src="https://img.shields.io/badge/pandas-%23150458.svg?style=for-the-badge&logo=pandas&logoColor=white" alt="Pandas">
          <img src="https://img.shields.io/badge/NumPy-013243?style=for-the-badge&logo=numpy&logoColor=white" alt="NumPy">
          <img src="https://img.shields.io/badge/Matplotlib-%23ffffff.svg?style=for-the-badge&logo=Matplotlib&logoColor=black" alt="Matplotlib">
          <img src="https://img.shields.io/badge/Plotly-%233F4F75.svg?style=for-the-badge&logo=plotly&logoColor=white" alt="Plotly">
        </div>
      </div>
      
      <!-- Tools & Platforms -->
      <div class="card" style="padding: 2rem;">
        <h3 style="font-size: 1.5rem; font-weight: 700; margin-bottom: 1.5rem; display: flex; align-items: center; gap: 0.5rem;">
          <i class="fa-solid fa-toolbox" style="color: var(--primary-color, #2563eb);"></i>
          Tools & Platforms
        </h3>
        <div style="display: flex; flex-wrap: wrap; gap: 0.75rem;">
          <img src="https://img.shields.io/badge/git-%23F05033.svg?style=for-the-badge&logo=git&logoColor=white" alt="Git">
          <img src="https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white" alt="Docker">
          <img src="https://img.shields.io/badge/Jupyter-F37626?style=for-the-badge&logo=jupyter&logoColor=white" alt="Jupyter">
          <img src="https://img.shields.io/badge/LaTeX-008080?style=for-the-badge&logo=latex&logoColor=white" alt="LaTeX">
        </div>
      </div>
    </div>
  </div>
</section>

<!-- Call to Action Section -->
<section class="section text-center" style="background: linear-gradient(135deg, #2563eb 0%, #06b6d4 100%); color: white;">
  <div class="container-sm">
    <h2 style="font-size: 3rem; font-weight: 800; margin-bottom: 1rem;">Interested in Collaborating?</h2>
    <p style="font-size: 1.25rem; margin-bottom: 2rem; opacity: 0.95;">
      I'm always open to discussing research opportunities, consulting projects, or teaching collaborations in AI and machine learning.
    </p>
    <div style="display: flex; gap: 1rem; justify-content: center; flex-wrap: wrap;">
      <a href="mailto:chantelatta@gmail.com" class="btn btn-accent btn-lg">
        <i class="fa-solid fa-envelope"></i> Get in Touch
      </a>
      <a href="/Resume/" class="btn btn-outline btn-lg" style="border-color: white; color: white;">
        <i class="fa-solid fa-file-lines"></i> View Resume
      </a>
    </div>
  </div>
</section>

</div>

{% include back-to-top.html %}

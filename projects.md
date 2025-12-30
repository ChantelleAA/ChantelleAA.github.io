---
layout: page
title: Projects
permalink: /projects/
---

<div class="page-hero">
  <div class="container">
    <h1 class="page-title">Projects</h1>
    <p class="page-subtitle">AI systems, research prototypes, and production applications spanning climate science, education technology, healthcare, and political analytics</p>
  </div>
</div>

<section class="section">
  <div class="container-lg">
    {% include filter-bar.html 
       categories="ML/AI,Web Apps,Research,Education"
       placeholder="Search projects by name or technology..."
       filter_type="projects"
    %}
    
    <!-- Featured Projects Section -->
    <div class="featured-projects">
      <h2 class="section-title" style="margin-top: 3rem;">Featured Projects</h2>
      
      <div class="projects-grid">
        <!-- Project 1: Kola Market AI Systems -->
        <div data-filterable="projects" data-category="ml-ai" data-title="Kola Market AI Systems" data-tags="Python Django LangChain OCR SQL" data-date="2025">
          {% include project-card.html
             title="Kola Market AI Systems"
             description="Lead AI/ML Engineer building production ML systems for African MSME marketplace. Inventory recommendation engine using internal and external data sources, OCR/data-capture for field sales, credit-scoring for MSMEs, and WhatsApp LLM agent integration."
             tech_stack="Python,Django,LangChain,OCR,SQL"
             date="Dec 2025 - Present"
             status="In Production"
             category="ML/AI"
             featured=true
          %}
        </div>
        
        <!-- Project 2: Quantathon Judging Platform -->
        <div data-filterable="projects" data-category="web-apps" data-title="Quantathon Judging Platform" data-tags="Django PostgreSQL HTMX Railway" data-date="2025">
          {% include project-card.html
             title="Quantathon Judging Platform"
             description="Django-based hackathon judging system used in AIMS Quantathon 2025. Real-time leaderboard and analytics, secure voting system, criteria filtered by judge expertise. Mentored winning team who developed quantum-inspired malaria drug discovery model."
             image="/assets/images/projects/judging_demo.gif"
             tech_stack="Django,PostgreSQL,HTMX,Railway"
             github_url="https://github.com/ChantelleAA/judging_criteria"
             date="Jul 2025"
             impact="50+ participants, successful event management"
             category="Web Apps"
             featured=true
          %}
        </div>
        
        <!-- Project 3: TLR Helper -->
        <div data-filterable="projects" data-category="education" data-title="TLR Helper Ghana Curriculum" data-tags="Django HTMX PostgreSQL Bootstrap5 Pinterest" data-date="2025">
          {% include project-card.html
             title="TLR Helper"
             description="Ghana Standards-Based Curriculum platform with 500+ teaching resources. Multi-level search system (Class, Subject, Term, Strand, Standard, Indicator), Pinterest API integration, and offline PDFs. Used in TEDD Ghana workshops."
             image="/assets/images/projects/tlr_helper_1.gif"
             tech_stack="Django,HTMX,PostgreSQL,Bootstrap5,Pinterest API"
             github_url="https://github.com/ChantelleAA/tlr_app"
             date="Jun 2025"
             impact="Used in TEDD Ghana teacher workshops"
             category="Education"
             featured=true
          %}
        </div>
      </div>
    </div>
    
    <!-- All Projects Grid -->
    <h2 class="section-title" style="margin-top: 4rem;">All Projects</h2>
    
    <div class="projects-grid" data-filter-container="projects">
      <!-- Research Projects -->
      
      <!-- Brain Tumor Segmentation -->
      <div data-filterable="projects" data-category="research" data-title="Brain Tumor Segmentation MICCAI" data-tags="PyTorch MONAI Medical-Imaging NumPy" data-date="2024">
        {% include project-card.html
           title="Brain Tumor Segmentation (MICCAI)"
           description="Ensemble models for Sub-Saharan MRI data segmentation. MICCAI 2023 Scholarship recipient. Proposed new methods (Staple Assembling & Mednex) for improved outcomes on limited medical imaging datasets."
           image="/assets/images/projects/bts_img.png"
           tech_stack="PyTorch,MONAI,NumPy,Python"
           paper_url="https://arxiv.org/abs/2508.10905"
           date="May 2024 - Aug 2024"
           impact="International conference presentation"
           category="Research"
        %}
      </div>
      
      <!-- GeoSeg Biodiversity -->
      <div data-filterable="projects" data-category="research" data-title="GeoSeg Biodiversity Segmentation" data-tags="PyTorch UNetFormer FT-UNetFormer DCSwin GeoPandas" data-date="2024">
        {% include project-card.html
           title="GeoSeg Biodiversity Segmentation"
           description="Led geospatial AI work for ODOS Tech. Improved mIoU from 68-72% to 87-90% using knowledge distillation framework. Sentinel/OpenEarthMap satellite imagery processing for land cover classification."
           image="/assets/images/projects/biodiversity.gif"
           tech_stack="PyTorch,UNetFormer,FT-UNetFormer,DCSwin,GeoPandas"
           github_url="https://github.com/ChantelleAA/geoseg"
           date="2024"
           impact="87-90% mIoU (from 68-72%)"
           category="Research"
        %}
      </div>
      
      <!-- RTE Energy Research -->
      <div data-filterable="projects" data-category="research" data-title="RTE Pollution Dashboard Climate AI" data-tags="Streamlit GeoPandas Plotly Pandas" data-date="2024">
        {% include project-card.html
           title="RTE Energy Research - Pollution Dashboard"
           description="Multi-city pollution analytics for RTE Investigates renewable energy story. Satellite bounding box extraction + ground sensor fusion for air-quality analysis across multiple Chinese cities."
           image="/assets/images/projects/air-quality-app.gif"
           tech_stack="Streamlit,GeoPandas,Plotly,Pandas"
           github_url="https://github.com/ChantelleAA/urumqi_analysis"
           date="2024"
           category="Research"
        %}
      </div>
      
      <!-- Oware RL -->
      <div data-filterable="projects" data-category="research" data-title="Oware Reinforcement Learning DQN" data-tags="Python TensorFlow Stable-Baselines RL" data-date="2024">
        {% include project-card.html
           title="Oware Nam-nam Reinforcement Learning"
           description="DQN, DDQN, A3C, and AlphaZero implementations for traditional African game. Custom game environment with human-vs-agent and agent-vs-agent modes. LUT University Master's thesis project."
           image="/assets/images/projects/oware_demo1.gif"
           tech_stack="Python,TensorFlow,Stable-Baselines"
           github_url="https://github.com/ChantelleAA/Reinforcement_Learning_Oware"
           paper_url="https://lutpub.lut.fi/bitstream/handle/10024/167861/mastersthesis_Amoako-Atta_Chantelle.pdf"
           date="Aug 2023 - Aug 2024"
           category="Research"
        %}
      </div>
      
      <!-- Cardiac Arrhythmia -->
      <div data-filterable="projects" data-category="research" data-title="Cardiac Arrhythmia ML Classifier" data-tags="scikit-learn XGBoost Python" data-date="2023">
        {% include project-card.html
           title="Cardiac Arrhythmia Classifier"
           description="ML algorithms for arrhythmia prediction from physiological signals. AIMS Rwanda Master's thesis using classical ML approaches and signal processing techniques."
           tech_stack="scikit-learn,XGBoost,Python"
           github_url="https://github.com/ChantelleAA/Cardiac_Arrhythmia_ML"
           date="Aug 2022 - Jun 2023"
           category="Research"
        %}
      </div>
      
      <!-- 3D LeapMotion -->
      <div data-filterable="projects" data-category="research" data-title="3D LeapMotion Digit Classification" data-tags="Python scikit-learn ANNs" data-date="2023">
        {% include project-card.html
           title="3D LeapMotion Digit Classification"
           description="99% accuracy with Artificial Neural Networks for 3D handwritten digit recognition from LeapMotion Sensor data. LUT University course project."
           tech_stack="Python,scikit-learn,ANNs"
           date="Oct 2023 - Dec 2023"
           category="Research"
        %}
      </div>
      
      <!-- ML/AI Applications -->
      
      <!-- Twitter Election Prediction -->
      <div data-filterable="projects" data-category="ml-ai" data-title="Twitter Election Prediction Sentiment Analysis" data-tags="Python Transformers BERT GPT LangChain" data-date="2025">
        {% include project-card.html
           title="Twitter Election Prediction"
           description="BERT/GPT sentiment analysis for political forecasting. 20% accuracy improvement by integrating metadata. End-to-end pipeline from data collection to real-time forecasting for Cape Wesley Consult."
           tech_stack="Python,Transformers,LangChain,Twitter API"
           date="Nov 2024 - Jan 2025"
           impact="20% accuracy improvement"
           category="ML/AI"
        %}
      </div>
      
      <!-- News Article Sentiment -->
      <div data-filterable="projects" data-category="ml-ai" data-title="News Article Political Sentiment NLP" data-tags="Python BERT SpaCy NLTK" data-date="2025">
        {% include project-card.html
           title="News Article Political Sentiment Analysis"
           description="NLP-based prediction model for political sentiment and election outcomes. Text processing (tokenization, NER) with fine-tuned Hugging Face models for Cape Wesley Consult."
           tech_stack="Python,BERT,SpaCy,NLTK"
           date="Nov 2024 - Jul 2025"
           category="ML/AI"
        %}
      </div>
      
      <!-- NileEdge AI Assistant -->
      <div data-filterable="projects" data-category="ml-ai" data-title="NileEdge AI Assistant Chatbot" data-tags="Python Flask ChromaDB Whisper" data-date="2024">
        {% include project-card.html
           title="NileEdge AI Assistant"
           description="Context-aware chatbot with semantic FAQ matching and Whisper transcription. Hybrid retrieval + LLM inference, privacy-first running entirely locally with custom UI."
           image="/assets/images/projects/nileedgechatbot.gif"
           tech_stack="Python,Flask,ChromaDB,Whisper"
           github_url="https://github.com/ChantelleAA/response_aigent"
           date="2024"
           category="ML/AI"
        %}
      </div>
      
      <!-- Case-Mediators Matching -->
      <div data-filterable="projects" data-category="ml-ai" data-title="Case-Mediators Matching System NLP" data-tags="Django Python NLP Transformers" data-date="2024">
        {% include project-card.html
           title="Case-Mediators Matching System"
           description="Django-based mediation platform with transformer-based matching. Dynamic forms for data capture. Ishango AI Hackathon award winner for streamlining case-mediation processes."
           tech_stack="Django,Python,NLP,Transformers"
           github_url="https://github.com/ChantelleAA/Matching_and_Scheduling_System"
           date="May 2024"
           impact="Ishango AI Hackathon Winner"
           category="ML/AI"
        %}
      </div>
      
      <!-- OCR Research -->
      <div data-filterable="projects" data-category="research" data-title="OCR Research Evaluation Benchmarking" data-tags="Python Tesseract EasyOCR PaddleOCR OpenCV" data-date="2025">
        {% include project-card.html
           title="OCR Research & Evaluation"
           description="Benchmarking OCR engines for document processing. Performance metrics comparison of Tesseract, EasyOCR, PaddleOCR with preprocessing pipeline optimization for improved accuracy."
           tech_stack="Python,Tesseract,EasyOCR,PaddleOCR,OpenCV"
           date="2024-2025"
           category="Research"
        %}
      </div>
      
      <!-- Education & Workshops -->
      
      <!-- GeoAI Workshop -->
      <div data-filterable="projects" data-category="education" data-title="GeoAI Workshop Satellite Imagery" data-tags="Python Jupyter GeoPandas Rasterio QGIS" data-date="2025">
        {% include project-card.html
           title="GeoAI Workshop Materials"
           description="Satellite imagery processing tutorials and land cover classification. Hands-on Jupyter notebooks for geospatial AI and environmental monitoring with Python."
           image="/assets/images/projects/geoai_workshop.gif"
           tech_stack="Python,Jupyter,GeoPandas,Rasterio,QGIS"
           github_url="https://github.com/ChantelleAA/gain_geoai_workshop"
           date="2025"
           category="Education"
        %}
      </div>
      
      <!-- Python Learning Materials -->
      <div data-filterable="projects" data-category="education" data-title="Python Learning Materials Teaching" data-tags="Python Jupyter" data-date="2024">
        {% include project-card.html
           title="Python Learning Materials"
           description="Teaching notebooks, scrapers, and educational visualizers for programming instruction. Resources used for teaching Python and data science to 200+ students."
           tech_stack="Python,Jupyter"
           github_url="https://github.com/ChantelleAA/Python-Learning-Materials"
           date="2024"
           category="Education"
        %}
      </div>
    </div>
    
    <!-- Stats Section -->
    <div class="projects-stats">
      <div class="stat-card">
        <span class="stat-number">15+</span>
        <span class="stat-label">Completed Projects</span>
      </div>
      <div class="stat-card">
        <span class="stat-number">8</span>
        <span class="stat-label">Research Publications</span>
      </div>
      <div class="stat-card">
        <span class="stat-number">6</span>
        <span class="stat-label">Production Systems</span>
      </div>
      <div class="stat-card">
        <span class="stat-number">5+</span>
        <span class="stat-label">Technologies Mastered</span>
      </div>
    </div>
    
    <!-- Call to Action -->
    <div class="cta-section">
      <h2>Interested in Collaborating?</h2>
      <p>I'm always open to discussing new projects, research opportunities, or ways to bring AI solutions to real-world problems.</p>
      <a href="mailto:chantelatta@gmail.com" class="btn btn-primary btn-lg">Get in Touch</a>
    </div>
  </div>
</section>

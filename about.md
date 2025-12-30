---
layout: page
title: About
permalink: /about/
---

<style>
.about-hero {
  background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
  color: white;
  padding: 5rem 2rem 4rem;
  margin: -2rem -2rem 3rem -2rem;
  text-align: center;
}

.hero-profile {
  max-width: 200px;
  margin: 0 auto 2rem;
}

.hero-profile img {
  width: 100%;
  border-radius: 50%;
  border: 6px solid rgba(255, 255, 255, 0.3);
  box-shadow: 0 10px 40px rgba(0, 0, 0, 0.3);
}

.about-hero h1 {
  font-size: 3rem;
  font-weight: 700;
  margin-bottom: 1rem;
  line-height: 1.2;
}

.about-hero .subtitle {
  font-size: 1.5rem;
  font-weight: 400;
  opacity: 0.95;
  margin-bottom: 1rem;
}

.about-hero .tagline {
  font-size: 1.1rem;
  font-weight: 300;
  opacity: 0.9;
  max-width: 700px;
  margin: 0 auto;
  line-height: 1.6;
}

.about-section {
  max-width: 800px;
  margin: 0 auto 3rem;
  padding: 0 2rem;
}

.about-section h2 {
  font-size: 2rem;
  font-weight: 700;
  color: #2c3e50;
  margin-bottom: 1.5rem;
  border-bottom: 3px solid #667eea;
  padding-bottom: 0.5rem;
  display: inline-block;
}

.about-section p {
  font-size: 1.1rem;
  line-height: 1.8;
  color: #555;
  margin-bottom: 1rem;
}

.about-section ul {
  list-style: none;
  padding: 0;
}

.about-section ul li {
  font-size: 1.05rem;
  line-height: 1.8;
  color: #555;
  margin-bottom: 0.75rem;
  padding-left: 1.5rem;
  position: relative;
}

.about-section ul li:before {
  content: "→";
  position: absolute;
  left: 0;
  color: #667eea;
  font-weight: bold;
}

.interests-grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 1.5rem;
  margin: 2rem 0;
}

.interest-item {
  background: white;
  border: 2px solid #e1e8ed;
  border-radius: 12px;
  padding: 1.5rem;
  text-align: center;
  transition: all 0.3s ease;
}

.interest-item:hover {
  transform: translateY(-5px);
  box-shadow: 0 8px 24px rgba(0,0,0,0.12);
  border-color: #667eea;
}

.interest-item i {
  font-size: 2.5rem;
  color: #667eea;
  margin-bottom: 0.75rem;
}

.interest-item h3 {
  font-size: 1.1rem;
  font-weight: 600;
  color: #2c3e50;
  margin: 0;
}

.education-timeline {
  position: relative;
  padding-left: 2rem;
  margin: 2rem 0;
}

.education-timeline:before {
  content: '';
  position: absolute;
  left: 0;
  top: 0;
  bottom: 0;
  width: 3px;
  background: #667eea;
}

.education-item {
  position: relative;
  margin-bottom: 2rem;
  padding-left: 2rem;
}

.education-item:before {
  content: '';
  position: absolute;
  left: -2rem;
  top: 0.5rem;
  width: 15px;
  height: 15px;
  border-radius: 50%;
  background: #667eea;
  border: 3px solid white;
  box-shadow: 0 0 0 3px #667eea;
}

.education-item h3 {
  font-size: 1.2rem;
  font-weight: 600;
  color: #2c3e50;
  margin-bottom: 0.25rem;
}

.education-item .degree {
  font-size: 1rem;
  color: #667eea;
  font-weight: 500;
  margin-bottom: 0.25rem;
}

.education-item .year {
  font-size: 0.9rem;
  color: #888;
  margin-bottom: 0.5rem;
}

.education-item p {
  font-size: 0.95rem;
  color: #666;
  line-height: 1.6;
}

.awards-grid {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  gap: 1.5rem;
  margin: 2rem 0;
}

.award-card {
  background: white;
  border: 2px solid #e1e8ed;
  border-radius: 12px;
  padding: 1.5rem;
  transition: all 0.3s ease;
}

.award-card:hover {
  transform: translateY(-3px);
  box-shadow: 0 6px 20px rgba(0,0,0,0.1);
  border-color: #667eea;
}

.award-card i {
  font-size: 2rem;
  color: #f59e0b;
  margin-bottom: 0.75rem;
}

.award-card h3 {
  font-size: 1.1rem;
  font-weight: 600;
  color: #2c3e50;
  margin-bottom: 0.5rem;
}

.award-card p {
  font-size: 0.95rem;
  color: #666;
  line-height: 1.6;
  margin: 0;
}

.impact-stats {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  gap: 1.5rem;
  margin: 2rem 0;
}

.stat-box {
  background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
  color: white;
  border-radius: 12px;
  padding: 2rem 1rem;
  text-align: center;
  box-shadow: 0 4px 15px rgba(102, 126, 234, 0.3);
}

.stat-box .number {
  font-size: 2.5rem;
  font-weight: 700;
  display: block;
  margin-bottom: 0.5rem;
  line-height: 1;
}

.stat-box .label {
  font-size: 0.95rem;
  opacity: 0.95;
  line-height: 1.4;
}

.cta-section {
  background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
  color: white;
  padding: 3rem 2rem;
  border-radius: 12px;
  text-align: center;
  margin: 3rem 0;
}

.cta-section h2 {
  font-size: 2rem;
  font-weight: 700;
  margin-bottom: 1rem;
  color: white;
  border: none;
  display: block;
}

.cta-section p {
  font-size: 1.1rem;
  opacity: 0.95;
  margin-bottom: 2rem;
  max-width: 600px;
  margin-left: auto;
  margin-right: auto;
  color: white;
}

.cta-buttons {
  display: flex;
  gap: 1rem;
  justify-content: center;
  flex-wrap: wrap;
}

.cta-button {
  background: white;
  color: #667eea;
  padding: 0.75rem 2rem;
  border-radius: 8px;
  text-decoration: none;
  font-weight: 600;
  font-size: 1rem;
  transition: all 0.2s ease;
  display: inline-flex;
  align-items: center;
  gap: 0.5rem;
}

.cta-button:hover {
  transform: translateY(-2px);
  box-shadow: 0 6px 20px rgba(0, 0, 0, 0.15);
}

.cta-button.secondary {
  background: rgba(255, 255, 255, 0.2);
  color: white;
  border: 2px solid white;
}

.cta-button.secondary:hover {
  background: rgba(255, 255, 255, 0.3);
}

@media (max-width: 768px) {
  .about-hero h1 {
    font-size: 2rem;
  }
  
  .about-hero .subtitle {
    font-size: 1.2rem;
  }
  
  .about-hero .tagline {
    font-size: 1rem;
  }
  
  .interests-grid {
    grid-template-columns: repeat(2, 1fr);
    gap: 1rem;
  }
  
  .awards-grid {
    grid-template-columns: 1fr;
    gap: 1rem;
  }
  
  .impact-stats {
    grid-template-columns: repeat(2, 1fr);
    gap: 1rem;
  }
  
  .cta-buttons {
    flex-direction: column;
    align-items: stretch;
  }
  
  .cta-button {
    width: 100%;
    justify-content: center;
  }
}
</style>

<div class="about-hero">
  <div class="hero-profile">
    <img src="{{ site.avatar }}" alt="Chantelle Amoako-Atta">
  </div>
  <h1>Chantelle Amoako-Atta</h1>
  <p class="subtitle">PhD Researcher | ML Engineer | Educator</p>
  <p class="tagline">Building AI systems for climate resilience, healthcare, and education across Africa and beyond</p>
</div>

<div class="about-section">
  <h2>Who I Am</h2>
  <p>
    I'm a PhD researcher at University College Dublin working on AI for climate-resilient offshore wind energy, funded by the Met Eireann PhD Scholarship. I build machine learning systems that bridge the gap between research and real-world impact—from climate AI and geospatial analysis to NLP, computer vision, and healthcare applications.
  </p>
  <p>
    My work spans three core areas: advancing climate AI research, building production ML systems that solve real problems, and teaching the next generation of African AI practitioners. I believe that impactful AI must be both technically excellent and deeply connected to the communities it serves.
  </p>
</div>

<div class="about-section">
  <h2>Current Work</h2>
  <ul>
    <li><strong>PhD Research at UCD:</strong> Developing AI systems for optimizing offshore wind energy production in Irish waters, focusing on climate resilience, predictive maintenance, and energy forecasting using machine learning and remote sensing</li>
    <li><strong>Teaching & Mentorship:</strong> NLP lecturer at AIMS Ghana, teaching 200+ students across Africa in Python, data science, and AI. Deputy Sponsorship Committee Head for FemAfricMaths/Divas in AI program</li>
    <li><strong>Research & Consulting:</strong> Collaborating on climate AI, geospatial ML, NLP projects across academia and industry. MICCAI 2023 scholarship recipient for brain tumor segmentation research</li>
    <li><strong>Open Source & Community:</strong> Active contributor to Ghana NLP, building tools for Ghanaian languages and low-resource NLP</li>
  </ul>
</div>

<div class="about-section">
  <h2>Research Interests</h2>
  <div class="interests-grid">
    <div class="interest-item">
      <i class="fa-solid fa-wind"></i>
      <h3>Climate AI</h3>
    </div>
    <div class="interest-item">
      <i class="fa-solid fa-map"></i>
      <h3>Geospatial ML</h3>
    </div>
    <div class="interest-item">
      <i class="fa-solid fa-language"></i>
      <h3>NLP</h3>
    </div>
    <div class="interest-item">
      <i class="fa-solid fa-eye"></i>
      <h3>Computer Vision</h3>
    </div>
    <div class="interest-item">
      <i class="fa-solid fa-heart-pulse"></i>
      <h3>Healthcare AI</h3>
    </div>
    <div class="interest-item">
      <i class="fa-solid fa-graduation-cap"></i>
      <h3>Education Tech</h3>
    </div>
  </div>
</div>

<div class="about-section">
  <h2>Education</h2>
  <div class="education-timeline">
    <div class="education-item">
      <h3>University College Dublin</h3>
      <p class="degree">PhD in AI for Decarbonization (In Progress)</p>
      <p class="year">2024 - Present</p>
      <p>Met Eireann PhD Scholarship. Research focus: AI for climate-resilient offshore wind energy, predictive maintenance, and energy forecasting using machine learning and remote sensing.</p>
    </div>
    
    <div class="education-item">
      <h3>African Institute for Mathematical Sciences (AIMS) Rwanda</h3>
      <p class="degree">MSc in Mathematical Sciences</p>
      <p class="year">2019 - 2020</p>
      <p>Thesis: Machine Learning for Cardiac Arrhythmia Classification. Specialized in statistical learning, optimization, and signal processing for healthcare diagnostics.</p>
    </div>
    
    <div class="education-item">
      <h3>Lappeenranta University of Technology, Finland</h3>
      <p class="degree">MSc in Software Engineering and Digital Transformation</p>
      <p class="year">2020 - 2022</p>
      <p>Thesis: Playing Oware Nam-nam with Deep Q-Networks. Focus on reinforcement learning, game AI, and applying modern ML techniques to traditional games.</p>
    </div>
  </div>
</div>

<div class="about-section">
  <h2>Recognition & Awards</h2>
  <div class="awards-grid">
    <div class="award-card">
      <i class="fa-solid fa-award"></i>
      <h3>Met Eireann PhD Scholarship</h3>
      <p>Prestigious scholarship for AI research in climate and decarbonization at University College Dublin</p>
    </div>
    
    <div class="award-card">
      <i class="fa-solid fa-trophy"></i>
      <h3>MICCAI 2023 Scholar</h3>
      <p>International scholarship to present brain tumor segmentation research at premier medical imaging conference</p>
    </div>
    
    <div class="award-card">
      <i class="fa-solid fa-medal"></i>
      <h3>Ishango AI Hackathon Winner</h3>
      <p>Led team to victory building intelligent case-mediator matching system for legal disputes</p>
    </div>
    
    <div class="award-card">
      <i class="fa-solid fa-star"></i>
      <h3>SIAM Hackathon Winner</h3>
      <p>Led team to victory in Society for Industrial and Applied Mathematics competition</p>
    </div>
  </div>
</div>

<div class="about-section">
  <h2>Teaching & Impact</h2>
  <div class="impact-stats">
    <div class="stat-box">
      <span class="number">200+</span>
      <span class="label">Students Taught</span>
    </div>
    <div class="stat-box">
      <span class="number">5</span>
      <span class="label">Publications</span>
    </div>
    <div class="stat-box">
      <span class="number">15+</span>
      <span class="label">Projects</span>
    </div>
    <div class="stat-box">
      <span class="number">3</span>
      <span class="label">Hackathon Wins</span>
    </div>
  </div>
  <p>
    Teaching is at the heart of my work. As an NLP lecturer at AIMS Ghana, I delivered an intensive 2-week graduate-level course covering modern NLP techniques. I've taught Python, data science, and machine learning to over 200 students across universities (AIMS, Adaire School of AI) and professional training programs. Through FemAfricMaths and Divas in AI, I mentor early-career African women in mathematics and AI, serving as Deputy Sponsorship Committee Head.
  </p>
  <p>
    I also create and share educational resources—from GeoAI workshop materials on satellite imagery processing to Python learning notebooks used by hundreds of students. My goal is to make AI education accessible and empowering, especially for underrepresented communities in tech.
  </p>
</div>

<div class="about-section">
  <h2>Beyond Work</h2>
  <p>
    Outside of research and teaching, I enjoy quiet walks in nature, playing Oware (a traditional African board game that inspired my Master's thesis!), and connecting with people who share a love for curiosity and purposeful growth. I believe that the best ideas often come from unexpected conversations and diverse perspectives.
  </p>
</div>

<div class="cta-section">
  <h2>Let's Collaborate</h2>
  <p>
    I'm open to research collaborations, speaking engagements, consulting opportunities, and mentorship. Whether you're working on climate AI, building ML systems for social good, or looking for technical guidance—let's connect!
  </p>
  <div class="cta-buttons">
    <a href="mailto:chantelatta@gmail.com" class="cta-button">
      <i class="fa-solid fa-envelope"></i> Email Me
    </a>
    <a href="https://linkedin.com/in/chantelleaa" class="cta-button secondary" target="_blank" rel="noopener">
      <i class="fa-brands fa-linkedin"></i> Connect on LinkedIn
    </a>
    <a href="https://github.com/ChantelleAA" class="cta-button secondary" target="_blank" rel="noopener">
      <i class="fa-brands fa-github"></i> View GitHub
    </a>
  </div>
</div>

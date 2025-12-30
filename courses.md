---
layout: page
title: Courses & Workshops
permalink: /courses/
---

<div class="courses-page">
  <div class="page-header">
    <h1>Courses & Workshops</h1>
    <p class="page-subtitle">Teaching & Educational Content</p>
    <p>I believe in learning by building. Every lesson connects to a real project you'll complete, debug, and improve. These materials reflect my teaching experience with 200+ students across Africa.</p>
  </div>

  <!-- Python Fundamentals Course -->
  <section class="course-section">
    <div class="course-header">
      <h2>Python Fundamentals: 5 Project-Based Lessons</h2>
      <p class="course-description">Master Python through real-world projects. From temperature converters to text analytics tools, each lesson creates something you can use and share.</p>
    </div>

    <div class="course-stats">
      <div class="stat">
        <span class="stat-number">5</span>
        <span class="stat-label">Hands-On Lessons</span>
      </div>
      <div class="stat">
        <span class="stat-number">5</span>
        <span class="stat-label">Complete Projects</span>
      </div>
      <div class="stat">
        <span class="stat-number">100%</span>
        <span class="stat-label">Free Access</span>
      </div>
    </div>

    <div class="lesson-grid">
      {% assign python_posts = site.posts | where_exp: "post", "post.categories contains 'python-course'" | sort: 'order' %}
      {% for post in python_posts %}
        <div class="lesson-card">
          <div class="lesson-header">
            <span class="lesson-number">Lesson {{ post.order | default: forloop.index }}</span>
            <span class="lesson-difficulty">{{ post.difficulty | default: 'Beginner' }}</span>
          </div>
          
          <h3 class="lesson-title">{{ post.lesson_title | default: post.title }}</h3>

          <div class="lesson-concepts">{{ post.concepts | default: 'Core Python Concepts' }}</div>
          
          <div class="lesson-description">
            {{ post.excerpt | strip_html | truncatewords: 20 }}
          </div>
          
          <div class="lesson-footer">
            <span class="lesson-time">{{ post.duration | default: '20-25 min' }}</span>
            <a href="{{ post.url | prepend: site.baseurl }}" class="lesson-link">Start Lesson →</a>
          </div>
        </div>
      {% endfor %}
    </div>

    <div class="course-approach">
      <h3>Why Project-Based Learning Works</h3>
      <div class="approach-grid">
        <div class="approach-card">
          <h4>Immediate Results</h4>
          <p>See your code work from lesson one. Build confidence through working applications, not abstract exercises.</p>
        </div>
        <div class="approach-card">
          <h4>Real-World Skills</h4>
          <p>Learn patterns and practices used in professional development. Code that follows industry standards.</p>
        </div>
        <div class="approach-card">
          <h4>Portfolio Ready</h4>
          <p>Each project becomes part of your coding portfolio. Demonstrate your skills with actual applications.</p>
        </div>
      </div>
    </div>
  </section>

  <!-- Workshops Section -->
  <section class="workshops-section">
    <h2>Workshops & Lectures</h2>
    <p class="section-intro">I've delivered intensive courses and workshops on NLP, geospatial AI, and data science across African institutions.</p>
    
    <div class="workshops-grid">
      <div class="workshop-card">
        <div class="workshop-header">
          <h3>Natural Language Processing and Applications</h3>
          <span class="workshop-badge">2 Weeks</span>
        </div>
        <p class="workshop-location">African Institute for Mathematical Sciences (AIMS), Ghana</p>
        <p class="workshop-date">August - September 2025</p>
        <p class="workshop-description">Delivered intensive two-week course for Mastercard Foundation Transition Training Programme. Covered NLP fundamentals, transformers, and practical applications with Python.</p>
        <div class="workshop-topics">
          <span class="topic-pill">NLP</span>
          <span class="topic-pill">Transformers</span>
          <span class="topic-pill">BERT</span>
          <span class="topic-pill">Python</span>
        </div>
      </div>

      <div class="workshop-card">
        <div class="workshop-header">
          <h3>GeoAI Workshop: Satellite Imagery Processing</h3>
          <span class="workshop-badge">Workshop</span>
        </div>
        <p class="workshop-location">AIMS Ghana</p>
        <p class="workshop-date">2025</p>
        <p class="workshop-description">Hands-on workshop on geospatial AI and land cover classification using satellite imagery. Jupyter notebooks covering GeoPandas, Rasterio, and QGIS integration.</p>
        <div class="workshop-topics">
          <span class="topic-pill">GeoPandas</span>
          <span class="topic-pill">Rasterio</span>
          <span class="topic-pill">QGIS</span>
          <span class="topic-pill">Sentinel</span>
        </div>
      </div>

      <div class="workshop-card">
        <div class="workshop-header">
          <h3>Data Science & Machine Learning</h3>
          <span class="workshop-badge">Ongoing</span>
        </div>
        <p class="workshop-location">Adaire Academy, Ghana</p>
        <p class="workshop-date">September 2024 - Present</p>
        <p class="workshop-description">Instructing pilot program based on EPFL curriculum. Covering data analysis, visualization, R programming, Tidyverse, and ML concepts with real-world capstone projects.</p>
        <div class="workshop-topics">
          <span class="topic-pill">R</span>
          <span class="topic-pill">Tidyverse</span>
          <span class="topic-pill">Data Visualization</span>
          <span class="topic-pill">ML</span>
        </div>
      </div>
    </div>
  </section>

  <!-- Teaching Philosophy -->
  <section class="teaching-philosophy">
    <h2>Teaching Philosophy</h2>
    <div class="philosophy-content">
      <p>My teaching philosophy centers on <strong>learning by building</strong>. After teaching Python and data science to over 200 students at universities across Africa and building production ML systems, I've seen what works: practical, project-based learning that connects theory to real applications.</p>
      
      <p>Every concept I teach connects to a project students will complete, debug, and improve. No theoretical fluff—just practical skills that prepare learners for real development work. This approach has helped students land roles in data science, ML engineering, and research positions.</p>
      
      <p>Whether teaching NLP at AIMS Ghana, data science at Adaire Academy, or mentoring through FemAfricMaths, I focus on building confidence through immediate results and portfolio-ready projects.</p>
    </div>
  </section>

  <!-- CTA Section -->
  <section class="courses-cta">
    <h2>Want Me to Teach at Your Institution?</h2>
    <p>I'm available for workshops, guest lectures, and curriculum development in Python, machine learning, NLP, and geospatial AI.</p>
    <div class="cta-buttons">
      <a href="mailto:chantelatta@gmail.com" class="btn btn-primary btn-lg">Email Me</a>
      <a href="/about/" class="btn btn-outline btn-lg">Learn More About Me</a>
    </div>
  </section>
</div>

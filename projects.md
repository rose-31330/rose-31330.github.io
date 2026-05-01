---
layout: page
title: Projects
subtitle: Engineering and research projects
permalink: /projects/
---

  <div class="filter-bar">
    <button class="filter-btn active" data-filter="all">All</button>
    <button class="filter-btn" data-filter="competition">Competition</button>
    <button class="filter-btn" data-filter="research">Research</button>
    <button class="filter-btn" data-filter="coursework">Coursework</button>
    <button class="filter-btn" data-filter="team-project">Team Project</button>
    <button class="filter-btn" data-filter="individual-project">Individual</button>
  </div>

  <div class="projects-grid" id="projects-grid">

    <div class="project-card" data-tags="competition team-project">
      <!-- To add an image: <img src="/assets/images/rocketry.jpg" alt="Rocketry" class="project-img"> -->
      <div class="project-body">
        <div class="project-header">
          <h2>UKSEDS National Rocketry Championship</h2>
          <div class="tag-group">
            <span class="project-tag">Competition</span>
            <span class="project-tag">Team Project</span>
          </div>
        </div>
        <p class="project-meta">July 2025 – Present · QMUL Students for the Exploration and Development of Space</p>
        <p>Leading a team of 12 students to design, build, and launch a mid-power rocket to a target altitude with a unique payload, under strict competition guidelines.</p>
        <ul>
          <li>Applied systems engineering to integrate propulsion, avionics, structures, and recovery subsystems</li>
          <li>Overseeing full-cycle development: component selection, modelling, assembly, testing, and simulation</li>
          <li>Tools: Python, OpenRocket</li>
          <li>Managing outreach for QMSEDS including social media and conference events</li>
        </ul>
      </div>
    </div>

    <div class="project-card" data-tags="research team-project">
      <!-- To add an image: <img src="/assets/images/cubesat.jpg" alt="CubeSat" class="project-img"> -->
      <div class="project-body">
        <div class="project-header">
          <h2>QMSAT S.C.R.A.P. — Space Debris CubeSat</h2>
          <div class="tag-group">
            <span class="project-tag">Research</span>
            <span class="project-tag">Team Project</span>
          </div>
        </div>
        <p class="project-meta">June 2025 – Present · QMSAT / ESA collaboration</p>
        <p>Contributing to the mission concept definition of a 3U CubeSat to track and classify space debris using machine learning.</p>
        <ul>
          <li>Participated in the first ESA-sponsored Space Debris Hackathon at Technische Universität Berlin</li>
          <li>Selected for the ESA CubeSat Concurrent Engineering Workshop — trajectory &amp; mission analysis team</li>
          <li>Used model-based engineering tool COMET; applied requirements analysis and system-level trade-offs</li>
          <li>Constraints: 3U form factor, mass, power, and budget</li>
        </ul>
      </div>
    </div>

    <div class="project-card" data-tags="coursework team-project">
      <div class="project-body">
        <div class="project-header">
          <h2>Space Station Design for ADR - SDLR Orbit Determination and Prediction</h2>
          <div class="tag-group">
            <span class="project-tag">Coursework</span>
            <span class="project-tag">Team Project</span>
          </div>
        </div>
        <p class="project-meta">2025–2026 · QMUL Year 3 Design Project</p>
        <p>Year-long conceptual design of a space station for scalable active debris removal. Applied aerospace design principles and systems-level thinking across a multidisciplinary team. Individual design project focus: Improving orbit determination and prediction of space debris using Space Debris Laser Ranging (SDLR) with data sourced from ESA</p>
      </div>
    </div>

    <div class="project-card" data-tags="research individual-project">
      <div class="project-body">
        <div class="project-header">
          <h2>GNSS-R &amp; GNSS-SAR Technical Research</h2>
          <div class="tag-group">
            <span class="project-tag">Research</span>
            <span class="project-tag">Individual</span>
          </div>
        </div>
        <p class="project-meta">June–August 2025 · Satellite Applications Catapult · SPIN Programme</p>
        <p>Technical research into GNSS-Reflectometry and GNSS-based Synthetic Aperture Radar. Analysed data from CYGNSS, PRETTY, and HydroGNSS missions using Python.</p>
        <ul>
          <li>60+ page technical report synthesising literature, mission data, and commercial opportunity mapping</li>
          <li>Identified novel applications: peatland monitoring, flood risk, precision agriculture</li>
          <li>Mapped UK stakeholder landscape including UKSA, ESA, UKRI, SSTL, and Spire</li>
        </ul>
      </div>
    </div>

  </div>

<script>
  const buttons = document.querySelectorAll('.filter-btn');
  const cards   = document.querySelectorAll('.project-card');
  buttons.forEach(btn => {
    btn.addEventListener('click', () => {
      buttons.forEach(b => b.classList.remove('active'));
      btn.classList.add('active');
      const filter = btn.dataset.filter;
      cards.forEach(card => {
        card.style.display = (filter === 'all' || card.dataset.tags.includes(filter)) ? '' : 'none';
      });
    });
  });
</script>

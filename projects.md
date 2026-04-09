---
layout: page
title: Projects & Experience
subtitle: Filter by category to explore my work
permalink: /projects/
---

  <div class="filter-bar">
    <button class="filter-btn active" data-filter="all">All</button>
    <button class="filter-btn" data-filter="industrial-experience">Industrial Experience</button>
    <button class="filter-btn" data-filter="competition">Competition</button>
    <button class="filter-btn" data-filter="coursework">Coursework</button>
    <button class="filter-btn" data-filter="individual-project">Individual Project</button>
    <button class="filter-btn" data-filter="research">Research</button>
    <button class="filter-btn" data-filter="team-project">Team Project</button>
  </div>

  <div class="projects-grid" id="projects-grid">

    <div class="project-card" data-tags="industrial-experience research individual-project">
      <div class="project-header">
        <h2>Engineering Intern — Satellite Applications Catapult</h2>
        <div class="tag-group">
          <span class="project-tag">Industrial Experience</span>
          <span class="project-tag">Research</span>
        </div>
      </div>
      <p class="project-meta">Space Placements in Industry (SPIN) · June–August 2025 · Harwell Campus</p>
      <p>Conducted in-depth technical research into GNSS-Reflectometry and GNSS-based Synthetic Aperture Radar. Authored a 60+ page technical report synthesising literature and mission data analysis.</p>
      <ul>
        <li>Reviewed 40+ research papers on spaceborne missions, receiver design, and signal processing (DDMs, polarimetry, interferometry)</li>
        <li>Analysed mission data from CYGNSS, PRETTY, and HydroGNSS using Python</li>
        <li>Identified 3 novel commercial use cases: peatland monitoring, flood risk, precision agriculture</li>
        <li>Mapped 10+ key UK stakeholders including UKSA, ESA, UKRI, SSTL, and Spire</li>
        <li>Designed receiver architecture diagrams and processing flowcharts for internal presentations</li>
      </ul>
    </div>

    <div class="project-card" data-tags="competition team-project">
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

    <div class="project-card" data-tags="research team-project">
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

    <div class="project-card" data-tags="coursework team-project">
      <div class="project-header">
        <h2>Space Station Design for ISAM</h2>
        <div class="tag-group">
          <span class="project-tag">Coursework</span>
          <span class="project-tag">Team Project</span>
        </div>
      </div>
      <p class="project-meta">2024–2025 · QMUL Year 2 Design Project</p>
      <p>Year-long conceptual design of a space station for In-orbit Servicing, Assembly, and Manufacturing (ISAM). Applied aerospace design principles and systems-level thinking across a multidisciplinary team.</p>
    </div>

    <div class="project-card" data-tags="industrial-experience">
      <div class="project-header">
        <h2>President — Mile End Music Society</h2>
        <div class="tag-group">
          <span class="project-tag">Industrial Experience</span>
        </div>
      </div>
      <p class="project-meta">May 2024 – Present · Queen Mary University of London</p>
      <p>Leading one of QMUL's largest student societies (250 members), comprising six ensembles: Orchestra, Wind Band, Jazz Orchestra, Bands, Choir, and A Capella.</p>
      <ul>
        <li>Organised an inter-university Battle of the Bands — sold 300+ tickets; awarded Event of the Year at QM Student Group Awards 2025</li>
        <li>Planned concerts, liaised with venues and performers, managed repertoire</li>
        <li>Teaches classical piano, music theory, guitar, and bass through a student-led initiative</li>
      </ul>
    </div>

    <div class="project-card" data-tags="industrial-experience">
      <div class="project-header">
        <h2>Support Worker — QMUL Disability and Dyslexia Service</h2>
        <div class="tag-group">
          <span class="project-tag">Industrial Experience</span>
        </div>
      </div>
      <p class="project-meta">September 2024 – Present · Queen Mary University of London</p>
      <ul>
        <li>Assisted disabled students with access to university facilities, including laboratory activities</li>
        <li>Liaised with students with communication difficulties, conveying information clearly and concisely</li>
      </ul>
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
        if (filter === 'all' || card.dataset.tags.includes(filter)) {
          card.style.display = '';
        } else {
          card.style.display = 'none';
        }
      });
    });
  });
</script>

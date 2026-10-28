---
permalink: /
title: ""
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

<link rel="stylesheet" href="{{ '/assets/css/pubs.css' | relative_url }}">

I am an M.S. student in Electrical and Computer Engineering at UC San Diego, specializing in Intelligent Systems, Robotics & Control. Previously, I received my bachelor’s degree in Computer Science from the National University of Singapore.

My interests lie broadly in embodied AI, with a current focus on <strong>robot learning</strong> and <strong>dexterous manipulation</strong>. My experience spans manipulation benchmarks, learning-based methods, and real-world robot experiments. I am interested in building robotic systems that can perform tasks reliably in everyday environments and are intuitive for people to work with.

I am exploring PhD, research, and internship opportunities in robotics, and I welcome opportunities to collaborate. Please feel free to reach out!

Email: zhmu@ucsd.edu

## News
- **[Sep 2026]** <a href="https://nus-lins-lab.github.io/TROGrasp2Web/" style="text-decoration: none; border-bottom: none; box-shadow: none; color: #6baed6; "><strong>T(R,O) Grasp++</strong></a> was accepted to CoRL 2026!
- **[Sep 2026]** <a href="https://openreview.net/forum?id=LgUpMaBqCb" style="text-decoration: none; border-bottom: none; box-shadow: none; color: #6baed6;"><strong>ManiLadder</strong></a> was accepted to the IROS 2026 Workshop on Rethinking Bimanual Manipulation Beyond Single-Arm Policies and received the <span class="award-badge">Outstanding Paper Award</span>!
- **[Sep 2026]** A new chapter in San Diego⛵️🌵☀️! I began my M.S. in Electrical and Computer Engineering at UC San Diego, focusing on Intelligent Systems, Robotics & Control.
- **[Jun 2026]** Graduated from NUS with a Bachelor of Computing (Computer Science), Honours (Highest Distinction), and a Minor in Mathematics! 🦁🎓


## Publications & Preprints
<div class="pub-note"><sup>*</sup> equal contribution</div>

{% for p in site.data.publications %}
<div class="pub-card">
  <div class="pub-thumb">
    <img src="{{ p.img | relative_url }}" alt="{{ p.title }}">
  </div>
  <div class="pub-body">
    <h3 class="pub-title">{{ p.title }}</h3>
    <div class="pub-authors">
    {% for a in p.authors %}
      <span class="author{% if a.me %} me{% endif %}">
        {% if a.me %}<strong>{{ a.name }}</strong>{% else %}{{ a.name }}{% endif %}{% if a.equal %}<sup>*</sup>{% endif %}
      </span>{% unless forloop.last %}, {% endunless %}
    {% endfor %}
    </div>
    {% if p.venue %}
      <div class="pub-venue">{{ p.venue }}</div>
    {% endif %}

    {% if p.award %}
      <div class="pub-award">{{ p.award }}</div>
    {% endif %}
    {% if p.links %}
    <div class="pub-links">
      {% for l in p.links %}
        <a class="pub-link" href="{{ l.url | relative_url }}" target="_blank" rel="noopener">{{ l.text }}</a>
      {% endfor %}
    </div>
    {% endif %}
  </div>
</div>
{% endfor %}

<!-- ## SELECTED COURSEWORK
- **CS3263 Foundations of Artificial Intelligence:**
  Knowledge representation and reasoning with uncertainty; Bayesian networks; Markov Decision Process

- **CS4278 Intelligent Robots: Algorithms and Systems:**
  Kinematics; Theory and Models of Grasping; Motion Planning; State Estimation; Deep Reinforcement Learning

- **CS3210 Parallel Computing:**
  Theory of parallelism and models; shared-memory, distributed-memory, and data parallel architectures; CUDA and GPGPU programming -->

<!-- ## INTERNSHIP & WORK EXPERIENCE
* Research Intern, Agency For Science and Technology, CFAR, Singapore May 2024 - Aug 2024
  * Reproduced a diffusion-based dataset distillation baseline MinimaxDiffusion. 
  * Authored and deployed code for experimenting effect of mixing original and synthesized images.

* AI Intern, Tencent, Beijing, China Feb 2022 - Jun 2022
  * Proposed and implemented a solution to reduce false positive rates in Tencent Video AI-based Black/Blurred screen detection network; improved model's recall and accuracy by about 5% after deployment online.
  * Conducted in-depth research and experimentation on diverse loss functions and sampling methods for Tencent News' large-scale multi-label text classification network, leading to a 3% improvement in precision. -->

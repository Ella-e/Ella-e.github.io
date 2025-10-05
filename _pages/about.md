---
permalink: /
title: ""
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

I am a final year Computer Science undergradute at [School of Computing](https://www.comp.nus.edu.sg/), [National University of Singapore](https://www.nus.edu.sg/). 

With a passion in solving real-world problems, my research intersts lie in Embodied AI and Dexterous Manipulation. I am currently doing my Final Year Project about Robot Manipulation under the supervision of Prof. Lin SHAO. I’m actively seeking PhD opportunities beginning in August 2026 and am always open to new collaborations - please feel free to reach out~

Email: mu_zhaoyu@u.nus.edu

## SELECTED COURSEWORK
- **CS3263 Foundations of Artificial Intelligence:**
  Knowledge representation and reasoning with uncertainty; Bayesian networks; Markov Decision Process

- **CS4278 Intelligent Robots: Algorithms and Systems:**
  Kinematics; Theory and Models of Grasping; Motion Planning; State Estimation; Deep Reinforcement Learning

- **CS3210 Parallel Computing:**
  Theory of parallelism and models; shared-memory, distributed-memory, and data parallel architectures; CUDA and GPGPU programming

## INTERNSHIP & WORK EXPERIENCE
* Research Intern, Agency For Science and Technology, CFAR, Singapore May 2024 - Aug 2024
  * Explored diffusion-based dataset distillation methods.
  * Investigated the impact of mixing real and synthesized images on model performance.

* AI Intern, Tencent, Beijing, China Feb 2022 - Jun 2022
  * Proposed and implemented a solution to reduce false positive rates in Tencent Video AI-based Black/Blurred screen detection network; improved model's recall and accuracy by about 5% after deployment online.
  * Conducted in-depth research and experimentation on diverse loss functions and sampling methods for Tencent News' large-scale multi-label text classification network, leading to a 3% improvement in precision.

<link rel="stylesheet" href="{{ '/assets/css/pubs.css' | relative_url }}">
## Publications <div class="pub-note"><sup>*</sup> equal contribution</div>

{% for p in site.data.publications %}
<div class="pub-card">
  <div class="pub-thumb">
    <img src="{{ p.img | relative_url }}" alt="{{ p.title }}">
  </div>
  <div class="pub-body">
    <h3 class="pub-title">{{ p.title }}</h3>
    <div class="pub-authors">
    {% for a in p.authors %}
      <span class="author">
        {{ a.name }}{% if a.equal %}<sup>*</sup>{% endif %}
      </span>{% unless forloop.last %}, {% endunless %}
    {% endfor %}
    </div>
    {% if p.venue %}
      <div class="pub-venue">{{ p.venue }}</div>
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
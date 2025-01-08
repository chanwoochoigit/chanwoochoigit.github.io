---
layout: page
title: Experience
permalink: /experience/
description: Work experience, including both <code>research</code> and <code>industry</code> positions.
nav: true
nav_order: 3
display_categories: [Research, Industry]
horizontal: false
---

<div class="projects">
  {% for category in page.display_categories %}
    <h2 class="category">{{ category }}</h2>
    <div class="row row-cols-1 row-cols-md-2">
      {% for experience in site.data.resume.work %}
        {% if experience.category == category %}
          <div class="col mb-4">
            <div class="card h-100">
              <div class="card-body">
                <h5 class="card-title">{{ experience.position }}</h5>
                <p class="card-subtitle mb-2 text-muted">{{ experience.name }}</p>
                <p class="card-text">{{ experience.summary }}</p>
                {% if experience.url %}
                  <a href="{{ experience.url }}" class="card-link">Learn More</a>
                {% endif %}
              </div>
              <div class="card-footer">
                <small class="text-muted">{{ experience.startDate | date: "%B %Y" }} - {% if experience.endDate == "present" %}Present{% else %}{{ experience.endDate | date: "%B %Y" }}{% endif %}</small>
              </div>
            </div>
          </div>
        {% endif %}
      {% endfor %}
    </div>
  {% endfor %}
</div>
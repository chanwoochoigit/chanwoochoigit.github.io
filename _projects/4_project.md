---
layout: page
title: Recyclable Waste Classifier
description: Recyclable waste classification model with voting mechanisms, trained on multimodal sensor data
img: assets/img/rubbish.jpg
importance: 2
category: work
related_publications: true
---

As a data scientist intern, I contributed to a project focused on developing a deep neural network model for <code>classifying recyclable waste</code> into four categories: cans, clear PET bottles, opaque PET bottles, and glass bottles, given the multi-sensory data including pictures from 5 varying angles, weights, metal content, and object opacity. Inspired by research that employs <code>voting mechanisms</code> for multiclass classification {% cite zhang2020competitive %} {% cite leon2017evaluating %}, a similar <code>voting-based ensemble</code> was used for multiclass classification on multimodal sensor data.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/rubbish.png" title="Simplified Architecture of the multimodal deep neural network model for recyclable waste classification" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Simplified Architecture of the multimodal deep neural network model for recyclable waste classification
</div>

My primary responsibilities covered two key areas:
- 1) <code>data pipeline construction</code>, which included data collection, creating a data collection manual for crowdsourcing, and data preprocessing. 

- 2) <code>model development and evaluation</code>, which involved model design, training, and testing. The implementation was done using the <code>PyTorch</code> framework, <code>AWS ECS/EC2</code>, and <code>Docker</code>.
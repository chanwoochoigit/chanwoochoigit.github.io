---
layout: page
title: Residential Property Analytics
description: Deep neural network house prediction model - not to predict property prices, but to capture the set of PoIs that contribute most to the price
img: assets/img/realty.jpg
importance: 1
category: personal
related_publications: true
---

As a personal project, I worked on analysing the "important" point of interests (PoIs) that have the <code>most significant impact</code> on the <code>prices of individual residential properties and neighborhoods</code>. The motivation came from the general recognition that certain geographical factors, like proximity to large hospitals, universities, office buildings, department stores, parks, and national landmarks, influence the financial value of residential properties. However, the specific details and <code>relative importance of these different PoIs</code> were <code>not well understood</code>. The goal was to further investigate and identify which PoIs contribute the most to property prices. 

The training data included residential property prices, the surrounding PoIs, and the distances from each PoI to the target property. Dealing with the O(MN) complexity arising from the combinations of property prices, PoIs, and distances became a complicating factor in the computation.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/realty.png" title="Frontend Demo Image of AI Law Mentor, displaying multiple boolean values for relevant crimes that can be fed to the system using radio buttons" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Frontend Demo Image of AI Law Mentor, displaying multiple boolean values for relevant crimes that can be fed to the system using radio buttons
</div>

Key project components and findings: 

- A DNN model was trained to predict house prices given the surrounding PoIs and their distances to the target property.

- Explainable AI (XAI) approaches, such as Shapley values, were utilized to calculate the contribution of each PoI to residential property prices.

- Gradient boosting-based regression methods, including lightgbm and XGBoost, were employed to transparently assess the importance and contribution of surrounding PoIs.

- The analysis revealed a strong correlation between property prices and the distances to surrounding PoIs, regardless of the size or category of the PoI.

- Due to various limitations, a strong conclusion on which specific categories of PoIs and their quantified distance-based correlations impact property prices could not be established.

Future directions: 

- Constructing a more up-to-date and robust data pipeline.

- Incorporating domain knowledge as prior information in the neural network models, potentially through knowledge transfer techniques.

- Further analysis to quantify the impact of different PoI categories and their distances on residential property prices.
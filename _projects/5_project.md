---
layout: page
title: AI Law Mentor
description: Deep neural network regression model for sentencing prediction of criminal cases, based on court judgements
img: assets/img/law_mentor.jpg
importance: 1
category: work
related_publications: true
---

As a data scientist intern, I led a team of three to develop a <code>deep neural network regression</code> model for predicting <code>sentencing in criminal cases</code>. The project aimed to provide users with tools to <code>estimate potential sentences</code> when facing relevant <code>legal complications</code>. An ensemble of deep neural network models was employed to 1) map court judgments to word/document embeddings and 2) predict sentence durations. The model architecture was inspired by the works of {% cite virtucio2018predicting nay2018natural %}, while {% cite xiao2018cail2018 %} provided helpful guidance on data construction.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/law_mentor.png" title="Frontend Demo Image of AI Law Mentor, displaying multiple boolean values for relevant crimes that can be fed to the system using radio buttons" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Frontend Demo Image of AI Law Mentor, displaying multiple boolean values for relevant crimes that can be fed to the system using radio buttons
</div>

Key project components and my contributions: 

- Data pipeline construction: Collected and preprocessed 16,000 court judgment data points. 

- Implementation: Conducted relevant research survey, designed and implemented models, trained models, and built a backend server for real-time inference. 

- Evaluation: Achieved 84% accuracy in sentencing prediction, with a correct prediction defined as a difference of 6 months or less between the predicted and actual sentence.

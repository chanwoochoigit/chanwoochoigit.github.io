---
layout: page
title: LiAct
description: Live Physical Activity Monitoring App
img: assets/img/liact_thumbnail.jpg
importance: 2
category: uni
related_publications: true
---

As a 4th year project for the course <code>Principles and Design of IoT Systems</code>, I worked in a team of 2 to build a live physical activity monitoring app given a series of  gyrosensory data using a neural <code>network body posture classification</code> model. The model classifies human body posture near-real-time and records the results to generate a 24-hour report of physical activity level. We designed the app to alert users aged 65 or more to stay active and maintain good health. I was primarily responsible for developing the classifier using <code>Tensorflow</code> and integrating it with the Android app using <code>Firebase</code> for database hosting.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/liact_pg1.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/liact_pg2.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/liact_pg3.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    LiAct application user interface. (Left) The landing page of the application. (Center) A 24-hour activity level report visualized using a donut chart (demonstrated on a shorter time period for illustrative purposes). (Right) The data adjustment page designed to hypothetically track and compare the results of peer users with similar age and health conditions.
</div>

The key takeaways of the project and my contributions are:

- Implemented a time series classifier that distinguishes 4 types of activities the wearer is currently performing, using an IoT device that measures the wearer's degree of movement as time series data

- Developed a healthcare app that assesses the level of activity during daily life, targeting users aged 65 and above, and conducted a demo day

- Converted the trained and tested deep learning model into a TF Lite model to enable live classification and service in a mobile environment, and deployed it on a Firebase server

- In a 2-person project, took charge of developing the live time series data classifier deep learning model, model optimization, and Firebase integration

- Achieved over 90% accuracy and F1-score


<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/liact_architecture.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Basic architecture of LiAct. The RESpeck device {% cite arvind2021home %} was provided by the course administrator for academic use.
</div>

Not as expected, it was empirically discovered that the CNN with skip-connection enabled model recorded a much worse classification f1-score compared to a much simpler DNN with 3 hidden layers. This demonstrates that, as [David Wolpert](https://www.santafe.edu/people/profile/david-wolpert)'s <code>No Free Lunch</code> theorem {% cite wolpert1997no %}  implies, more complex models with a large number of additional mechanisms do not guarantee better performance.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/liact_architecture2.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Much simpler 5-layer DNN outperforms CNN with Skip-connection by a significant margin
</div>
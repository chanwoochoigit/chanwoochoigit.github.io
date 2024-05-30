---
layout: page
title: E-Commerce Sales Forecaster
description: Sentence embedding-based YouTube subtitles search engine
img: assets/img/clips_ninja_thumbnail.jpg
importance: 1
category: template
related_publications: true
---

As a 5th year project for the course <code>Text Technologies for Data Science</code>, I led a team of 6 to build a <code>Youtube subtitles search engine</code> using a <code>Transformer Encoder</code> based sentence embedding module {% cite reimers2019sentence %} , finding the most relevant videos within the database of the subtitles of 250K videos. I was primarily in charge of constructing the <code>data pipeline</code>, <code>training & evaluating the ML model</code> and building the <code>back-end inference</code> module. 

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/clips_ninja_architecture.png" title="Clips Ninja backend & Inference Architecture" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Clips Ninja backend & Inference Architecture
</div>

The key takeaways of the project and my contributions are:

- Developed a natural language IR (Information Retrieval) search engine by vectorizing and creating a database of subtitles from 250,000 YouTube videos (in the education/information category) using the Sentence BERT library (6-person team project)

- As the team leader for the backend (server) part, conducted data collection, processing, database creation, and development of the search engine backend module

- Downloaded subtitles for 250,000 YouTube videos through API calls, processed subtitle data, used the Sentence BERT library for subtitle embedding, and stored them in a database as documents (~350GB)

- Designed and implemented Bi-level clustering for the search engine module

- Implemented query intake and result return modules

- Reduced search time from around 12 seconds to 0.8 - 1.2 seconds by implementing Bi-level clustering and a cold start prevention module

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/clips_ninja_thumbnail.png" title="Clips Ninja Frontent Image with search results" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Clips Ninja Frontent Image with search results
</div>

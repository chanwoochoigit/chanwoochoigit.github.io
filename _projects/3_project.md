---
layout: page
title: Bachelor's Dissertation
description: Personalised Privacy Policy statements using word embedding and neural network classifiers 
img: assets/img/bsc_thesis.jpg
importance: 3
category: uni
related_publications: true
---

For my Bachelor's final year dissertation, I developed a web application that classifies Privacy Policy (PP) statements and assesses the proportion of the document that could be considered potentially concerning based on the user's data privacy sensitivity persona. The objective of this work was to facilitate the reading and comprehension of PPs, as they are often extremely lengthy, leading to users rarely choosing to read them.

The neural network classifier underlying the web application was trained on a dataset of 50 Privacy Policies from the most-visited websites. Each Privacy Policy was divided into sentence chunks and annotated as either 'alarming' or 'less alarming' based on the given data sensitivity persona. Sentence Transformers {% cite reimers2019sentence %} were employed to map Privacy Policy sentences (or clauses) to embeddings and train the neural network classifier using the hand-annotated dataset of 1,200 Privacy Policy sentences corresponding to different persona scenarios.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/bsc_thesis.png" title="Frontent Demo Image with a company privacy policy (effective as of 4 February 2021) search results" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Frontent Demo Image with a company privacy policy (effective as of 4 February 2021
</div>

The key takeaways of the project and my contributions are:

- Designed and implemented a text classifier that categorizes sentences from privacy policy documents into important and unimportant based on three personas with different levels of data sensitivity

- Embedded privacy policy text collected from the web using Bag-of-Words (BoW) and BERT
Developed three types of text classifiers (DNN, CNN, and Transformer-based) using Tensorflow

- Achieved an average classification accuracy of 76.94% for persona-based classification (using the CNN model)

- Deployed the trained and tested deep learning model on a backend server and connected it with a simple frontend implementation to create a demo service for presentation

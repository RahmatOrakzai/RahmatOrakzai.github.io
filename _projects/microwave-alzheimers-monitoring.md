---

title: "Microwave Radar System for Non-Invasive Alzheimer’s Disease Monitoring"
collection: projects
date: 2023-01-01
excerpt: "A computational imaging and machine learning framework for monitoring neurodegenerative disease progression using microwave sensing technologies."
------------------------------------------------------------------------------------------------------------------------------------------------------------

<div style="text-align:center">
<img src="/images/PathalogicalModel.jpg" alt="Microwave antenna configuration around head model" width="520"/>
</div>

*Microwave antenna configuration and anatomical head model used for electromagnetic simulation and neurodegenerative disease monitoring.*

This research project investigated the development of **non-invasive microwave sensing and computational imaging techniques** for detecting and monitoring structural brain changes associated with neurodegenerative diseases such as Alzheimer’s disease and Parkinson’s disease.

The work integrates electromagnetic modelling, advanced signal processing, imaging algorithms, and machine learning approaches to enable longitudinal monitoring of disease progression without the need for expensive or invasive clinical imaging modalities such as MRI or CT.

The research explored pathological changes including brain atrophy, ventricular enlargement, and cerebrospinal fluid variations, and analysed how these structural changes affect microwave signal propagation through biological tissues. The resulting framework supports early diagnosis and scalable digital health monitoring solutions.

<div style="text-align:center">
<img src="/images/DMAS%20vs%20DAS.jpg" alt="DAS vs DMAS reconstruction comparison" width="600"/>
</div>

*Experimental phantom and reconstructed microwave imaging results comparing conventional Delay-and-Sum (DAS) with the proposed Delay-Multiply-and-Sum (DMAS) algorithm, illustrating enhanced contrast and localisation accuracy.*

---

## Key Contributions

* Development of microwave imaging algorithms for neurodegenerative disease detection
* Signal preprocessing and clutter removal techniques for biological measurements
* Frequency-domain and time-domain multistatic imaging approaches
* High-performance optimisation using distributed computing frameworks
* Machine learning-based classification of Alzheimer’s disease progression

---

## Technologies

Microwave imaging · Computational modelling · Machine learning · Biomedical signal processing · High-performance computing · Electromagnetic simulation

---

## PhD Thesis

**Data-driven microwave imaging and processing techniques for monitoring neurodegenerative diseases**
University of Edinburgh, United Kingdom, 2022

🔗 https://era.ed.ac.uk/items/c69550d7-7e72-4a1c-b3b3-d34d2b8cc300

---

## Research Datasets

**Experimental radar data for monitoring brain atrophy progression**
Biomedical dataset supporting microwave neuroimaging research

**Microwave sensing dataset for non-invasive monitoring of ventricle enlargement due to Alzheimer’s disease**
Open dataset for disease progression analysis

---

## External Project Link

🔗 https://ewireless.eng.ed.ac.uk/processing-and-imaging-techniques-microwave-based-neurodegenerative-diseases-detection

---

## Related Publications

{% assign related = site.publications | where: "project", "microwave-alzheimers" | sort: "date" | reverse %}

{% for post in related %}
{% include archive-single.html %}
{% endfor %}

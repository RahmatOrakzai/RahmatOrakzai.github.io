---
title: "Microwave Radar System for Non-Invasive Alzheimer’s Disease Monitoring"
collection: projects
date: 2023-01-01
excerpt: "A computational imaging and machine learning framework for monitoring neurodegenerative disease progression using microwave sensing technologies."
---

![Microwave antenna configuration around head model](/images/PathalogicalModel.jpg)

*Microwave antenna configuration and anatomical head model used for electromagnetic simulation and neurodegenerative disease monitoring.*

This research project investigated the development of **non-invasive microwave sensing and computational imaging techniques** for detecting and monitoring structural brain changes associated with neurodegenerative diseases such as Alzheimer’s disease and Parkinson’s disease.

The work integrates electromagnetic modelling, advanced signal processing, imaging algorithms, and machine learning approaches to enable longitudinal monitoring of disease progression without the need for expensive or invasive clinical imaging modalities such as MRI or CT.

The research explored pathological changes including brain atrophy, ventricular enlargement, and cerebrospinal fluid variations, and analysed how these structural changes affect microwave signal propagation through biological tissues. The resulting framework supports early diagnosis and scalable digital health monitoring solutions.

---

### Key Contributions

- Development of microwave imaging algorithms for neurodegenerative disease detection  
- Signal preprocessing and clutter removal techniques for biological measurements  
- Frequency-domain and time-domain multistatic imaging approaches  
- High-performance optimisation using distributed computing frameworks  
- Machine learning-based classification of Alzheimer’s disease progression  

---

### Technologies

Microwave imaging · Computational modelling · Machine learning · Biomedical signal processing · High-performance computing · Electromagnetic simulation

---

### External Project Link

🔗 https://ewireless.eng.ed.ac.uk/processing-and-imaging-techniques-microwave-based-neurodegenerative-diseases-detection

---

---

## Related Publications

{% assign related = site.publications | where: "project", "microwave-alzheimers" | sort: "date" | reverse %}

{% for post in related %}
{% include archive-single.html %}
{% endfor %}

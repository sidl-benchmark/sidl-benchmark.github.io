---
layout: project_page
permalink: /
title: "SIDL: A Real-World Dataset for Restoring Smartphone Images with Dirty Lenses"
venue: AAAI 2025
venue_url: https://aaai.org/conference/aaai/aaai-25/
authors:
    - name: Sooyoung Choi
      equal: true
    - name: Sungyong Park
      equal: true
    - name: Heewon Kim
affiliations:
    - name: Soongsil University
links:
    - name: Paper
      url: "#"
      note: "(Coming soon)"
    - name: Video
      url: "#"
      note: "(Coming soon)"
    - name: Code
      url: "#"
      note: "(Coming soon)"
    - name: Dataset
      url: "#"
      note: "(Coming soon)"
abstract: >
    Smartphone cameras are ubiquitous in daily life, yet their performance can be severely impacted by dirty lenses, leading to degraded image quality. This issue is often overlooked in image restoration research, which assumes ideal or controlled lens conditions. To address this gap, we introduced SIDL (Smartphone Images with Dirty Lenses), a novel dataset designed to restore images captured through contaminated smartphone lenses. SIDL contains diverse real-world images taken under various lighting conditions and environments. These images feature a wide range of lens contaminants, including water drops, fingerprints, and dust. Each contaminated image is paired with a clean reference image, enabling supervised learning approaches for restoration tasks. To evaluate the challenge posed by SIDL, various state-of-the-art restoration models were trained and compared on this dataset. Their performances achieved some level of restoration but did not adequately address the diverse and realistic nature of the lens contaminants in SIDL. This challenge highlights the need for more robust and adaptable image restoration techniques for restoring images with dirty lenses.
---

<!-- Title -->
<h1>{{ page.title }}</h1>

<!-- Authors -->
<div class="authors">
    {% for author in page.authors %}
        <span class="author">
            {{ author.name }}{% if author.equal %}*{% endif %}{% unless forloop.last %},{% endunless %}
        </span>
    {% endfor %}
</div>

<!-- Affiliations -->
<div class="affiliations">
    {% for affiliation in page.affiliations %}
        {{ affiliation.name }}{% unless forloop.last %}, {% endunless %}
    {% endfor %}
</div>

<!-- Links -->
<div class="links">
    {% for link in page.links %}
        <a href="{{ link.url }}" class="button">{{ link.name }}{{ link.note }}</a>
    {% endfor %}
</div>

<!-- Abstract -->
<div class="abstract">
    <h2>Abstract</h2>
    <p>{{ page.abstract }}</p>
</div>

---
layout: project_page
permalink: /
title: "SIDL: A Real-World Dataset for Restoring Smartphone Images with Dirty Lenses"
presentation: "AAAI 2025"
authors:
  - Sooyoung Choi*
  - Sungyong Park*
  - Heewon Kim
affiliations:
  - Soongsil University
paper: "https://your-link-to-paper.com"
video: "https://your-link-to-video.com"
code: "https://github.com/your-repo"
data: "https://github.com/your-repo/dataset"
---

<!-- Using HTML to center the abstract -->
<div class="columns is-centered has-text-centered">
  <div class="column is-four-fifths">
    <h2>Abstract</h2>
    <div class="content has-text-justified">
      Smartphone cameras are ubiquitous in daily life, yet their performance can be severely impacted by dirty lenses, leading to degraded image quality. This issue is often overlooked in image restoration research, which assumes ideal or controlled lens conditions. To address this gap, we introduced SIDL (Smartphone Images with Dirty Lenses), a novel dataset designed to restore images captured through contaminated smartphone lenses. SIDL contains diverse real-world images taken under various lighting conditions and environments. These images feature a wide range of lens contaminants, including water drops, fingerprints, and dust. Each contaminated image is paired with a clean reference image, enabling supervised learning approaches for restoration tasks. To evaluate the challenge posed by SIDL, various state-of-the-art restoration models were trained and compared on this dataset. Their performances achieved some level of restoration but did not adequately address the diverse and realistic nature of the lens contaminants in SIDL. This challenge highlights the need for more robust and adaptable image restoration techniques for restoring images with dirty lenses.
    </div>
  </div>
</div>

<div class = "comming soon">
  <h3>Comming Soon..</h3>
</div>

<!-- ## Background
The field of image restoration has mainly focused on ideal conditions, while real-world issues such as dirty smartphone lenses have been less explored. SIDL addresses this gap by providing a comprehensive set of images captured under real-world conditions with various types of lens contamination.

## Objective
The main goals of SIDL are:
- To provide a realistic benchmark for evaluating image restoration techniques.
- To challenge current methods with diverse and uncontrolled lens contaminations.
- To foster the development of adaptive and robust restoration algorithms.

## Key Ideas
- **Real-World Data Acquisition:** Images are captured in authentic environments with natural lens contaminants.
- **Paired Data:** Each dirty image is paired with its clean counterpart for supervised learning.
- **Evaluation Platform:** An online system is provided for real-time evaluation of submitted restoration results.

## Evaluate
Evaluation on the SIDL dataset includes both offline benchmarks and an online evaluation platform.  
Below, you can see real-time evaluation metrics (e.g., PSNR, SSIM):

<div id="evaluation-results">
  Loading evaluation results...
</div>

<script>
  // Example: Replace with your actual API endpoint
  async function fetchEvaluationResults() {
    try {
      const response = await fetch('https://api.example.com/evaluation-results');
      const data = await response.json();
      document.getElementById('evaluation-results').innerHTML = formatResults(data);
    } catch (error) {
      console.error('Error fetching evaluation results:', error);
      document.getElementById('evaluation-results').innerHTML = "Error loading evaluation results.";
    }
  }
  
  function formatResults(data) {
    let html = '<ul>';
    data.results.forEach(result => {
      html += `<li>${result.metric}: ${result.value}</li>`;
    });
    html += '</ul>';
    return html;
  }
  
  window.addEventListener('load', fetchEvaluationResults);
</script>

## Dataset
Download the SIDL dataset from the following link:

<a class="button is-primary" href="https://github.com/your-repo/dataset" target="_blank">Download Dataset</a>

## Image Acquisition Process
The images in the SIDL dataset were obtained using the following process:
1. **Capture Setup:** Images were captured under diverse lighting conditions to simulate realistic environments.
2. **Contaminant Application:** Natural contaminants such as water droplets, fingerprints, and dust were present during capture.
3. **Post-Processing:** Each image was paired with a clean reference after quality control.

![Image Acquisition](static/image/Turing_machine.png)

## Experiments
Below is a summary of experiments conducted on the SIDL dataset:

| Model         | PSNR  | SSIM  | Runtime (s) |
|---------------|-------|-------|-------------|
| Model A       | 28.5  | 0.85  | 0.5         |
| Model B       | 30.2  | 0.87  | 0.7         |
| Model C       | 27.8  | 0.83  | 0.6         |

## Citation -->

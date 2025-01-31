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

<!-- Hero Section with Background Image -->
<section class="hero is-fullheight is-info is-bold" style="background-image: url('static/image/your-background-image.jpg'); background-size: cover; background-position: center;">
  <div class="hero-body">
    <div class="container has-text-centered">
      <h1 class="title is-size-2-tablet is-size-1-desktop">
        SIDL: A Real-World Dataset for Restoring Smartphone Images with Dirty Lenses
      </h1>
      <h2 class="subtitle is-size-4-tablet is-size-3-desktop">
        AAAI 2025 | Soongsil University
      </h2>
      <div class="buttons is-centered">
        <a class="button is-primary is-large" href="#dataset">Download Dataset</a>
        <a class="button is-link is-large" href="#evaluation">Online Evaluation</a>
      </div>
    </div>
  </div>
</section>

<!-- Abstract Section -->
<section class="section">
  <div class="container">
    <div class="content has-text-centered">
      <h2 class="title">Abstract</h2>
      <p>
        Smartphone cameras are ubiquitous in daily life, yet their performance can be severely impacted by dirty lenses, leading to degraded image quality. This issue is often overlooked in image restoration research, which assumes ideal or controlled lens conditions. To address this gap, we introduced SIDL (Smartphone Images with Dirty Lenses), a novel dataset designed to restore images captured through contaminated smartphone lenses. SIDL contains diverse real-world images taken under various lighting conditions and environments. These images feature a wide range of lens contaminants, including water drops, fingerprints, and dust. Each contaminated image is paired with a clean reference image, enabling supervised learning approaches for restoration tasks. To evaluate the challenge posed by SIDL, various state-of-the-art restoration models were trained and compared on this dataset. Their performances achieved some level of restoration but did not adequately address the diverse and realistic nature of the lens contaminants in SIDL. This challenge highlights the need for more robust and adaptable image restoration techniques for restoring images with dirty lenses.
      </p>
    </div>
  </div>
</section>

<!-- Information Cards Section -->
<section class="section">
  <div class="container">
    <div class="columns is-multiline">
      <!-- Background Card -->
      <div class="column is-one-third">
        <div class="card">
          <header class="card-header">
            <p class="card-header-title">Background</p>
          </header>
          <div class="card-content">
            <div class="content">
              The field of image restoration has mainly focused on ideal conditions, while real-world issues such as dirty smartphone lenses have been less explored. SIDL fills this gap with authentic data.
            </div>
          </div>
        </div>
      </div>
      <!-- Objective Card -->
      <div class="column is-one-third">
        <div class="card">
          <header class="card-header">
            <p class="card-header-title">Objective</p>
          </header>
          <div class="card-content">
            <div class="content">
              <ul>
                <li>Provide a realistic benchmark for image restoration.</li>
                <li>Challenge current methods with diverse lens contaminants.</li>
                <li>Foster robust and adaptive restoration algorithms.</li>
              </ul>
            </div>
          </div>
        </div>
      </div>
      <!-- Key Ideas Card -->
      <div class="column is-one-third">
        <div class="card">
          <header class="card-header">
            <p class="card-header-title">Key Ideas</p>
          </header>
          <div class="card-content">
            <div class="content">
              <ul>
                <li><strong>Real-World Data Acquisition:</strong> Authentic capture conditions.</li>
                <li><strong>Paired Data:</strong> Dirty vs. clean images.</li>
                <li><strong>Evaluation Platform:</strong> Online real-time metrics.</li>
              </ul>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- Evaluate Section with Real-Time Results -->
<section class="section" id="evaluation">
  <div class="container">
    <h2 class="title has-text-centered">Evaluate</h2>
    <div id="evaluation-results" class="box">
      Loading evaluation results...
    </div>
    <script>
      // 실제 API 엔드포인트로 수정할 것
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
          html += `<li><strong>${result.metric}:</strong> ${result.value}</li>`;
        });
        html += '</ul>';
        return html;
      }
      
      window.addEventListener('load', fetchEvaluationResults);
    </script>
  </div>
</section>

<!-- Dataset Download Section -->
<section class="section" id="dataset">
  <div class="container has-text-centered">
    <h2 class="title">Dataset</h2>
    <p>Download the SIDL dataset from the link below:</p>
    <a class="button is-primary is-large" href="https://github.com/your-repo/dataset" target="_blank">Download Dataset</a>
  </div>
</section>

<!-- Image Acquisition Process Section -->
<section class="section">
  <div class="container">
    <h2 class="title has-text-centered">Image Acquisition Process</h2>
    <div class="columns is-vcentered">
      <div class="column is-half">
        <figure class="image is-4by3">
          <img src="static/image/Turing_machine.png" alt="Image Acquisition Process">
        </figure>
      </div>
      <div class="column is-half">
        <div class="content">
          <ol>
            <li><strong>Capture Setup:</strong> Images were captured under diverse lighting conditions.</li>
            <li><strong>Contaminant Application:</strong> Real-world contaminants (water droplets, fingerprints, dust) were naturally present during capture.</li>
            <li><strong>Post-Processing:</strong> Quality control ensured each dirty image is paired with a clean reference.</li>
          </ol>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- Experiments Section with Table -->
<section class="section">
  <div class="container">
    <h2 class="title has-text-centered">Experiments</h2>
    <div class="table-container">
      <table class="table is-striped is-fullwidth">
        <thead>
          <tr>
            <th>Model</th>
            <th>PSNR</th>
            <th>SSIM</th>
            <th>Runtime (s)</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <td>Model A</td>
            <td>28.5</td>
            <td>0.85</td>
            <td>0.5</td>
          </tr>
          <tr>
            <td>Model B</td>
            <td>30.2</td>
            <td>0.87</td>
            <td>0.7</td>
          </tr>
          <tr>
            <td>Model C</td>
            <td>27.8</td>
            <td>0.83</td>
            <td>0.6</td>
          </tr>
        </tbody>
      </table>
    </div>
  </div>
</section>

<!-- Citation Section -->
<section class="section">
  <div class="container">
    <h2 class="title has-text-centered">Citation</h2>
    <pre>
@inproceedings{anonymous2024sidl,
  title={{SIDL}: A Real-World Dataset for Restoring Smartphone Images with Dirty Lenses},
  author={Anonymous},
  booktitle={The 39th Annual AAAI Conference on Artificial Intelligence},
  year={2024},
  url={https://openreview.net/forum?id=oHKzYzEfIl}
}
    </pre>
  </div>
</section>

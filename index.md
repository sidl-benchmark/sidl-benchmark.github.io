---
layout: project_page
permalink: /
title: "SIDL: A Real-World Dataset for Restoring Smartphone Images with Dirty Lenses"
presentation: "AAAI 2025"
authors: "Sooyoung Choi*,   Sungyong Park*,   Heewon Kim"
affiliations:
  - Soongsil University
paper: "https://ojs.aaai.org/index.php/AAAI/article/view/32257"
video: "https://youtu.be/5nSJh-IPWd0"
code: "https://github.com/sidl-benchmark/sidl-benchmark.github.io"
data: "https://github.com/your-repo/dataset"
---

<style>
.gallery-wrapper {
  width: 100vw;
  margin-left: calc((100% - 100vw) / 2);
  display: grid;
  grid-template-columns: repeat(6, 1fr);
  grid-gap: 0;
  padding: 0;
}

.gallery-wrapper img {
  width: 100%;
  height: auto;
  display: block;
  transition: transform 0.3s ease;
  cursor: pointer;
}
.gallery-wrapper img:hover {
  transform: scale(1.3);
  z-index: 10;
}
</style>

<hr>

<div class="gallery-wrapper">
  <img src="images/Web_01_W.webp" alt="Example 001">
  <img src="images/Web_02_D.webp" alt="Example 002">
  <img src="images/Web_03_F.webp" alt="Example 003">
  <img src="images/Web_04_W.webp" alt="Example 004">
  <img src="images/Web_05_F.webp" alt="Example 005">
  <img src="images/Web_06_W.webp" alt="Example 006">
  <img src="images/Web_07_W.webp" alt="Example 007">
  <img src="images/Web_08_S.webp" alt="Example 008">
  <img src="images/Web_09_W.webp" alt="Example 009">
  <img src="images/Web_10_W.webp" alt="Example 010">
  <img src="images/Web_11_W.webp" alt="Example 011">
  <img src="images/Web_12_S.webp" alt="Example 012">
  <img src="images/Web_13_F.webp" alt="Example 013">
  <img src="images/Web_14_W.webp" alt="Example 014">
  <img src="images/Web_15_F.webp" alt="Example 015">
  <img src="images/Web_16_S.webp" alt="Example 016">
  <img src="images/Web_17_S.webp" alt="Example 017">
  <img src="images/Web_18_F.webp" alt="Example 018">
  <img src="images/Web_19_D.webp" alt="Example 019">
  <img src="images/Web_20_F.webp" alt="Example 020">
  <img src="images/Web_21_D.webp" alt="Example 021">
  <img src="images/Web_22_W.webp" alt="Example 022">
  <img src="images/Web_23_F.webp" alt="Example 023">
  <img src="images/Web_24_W.webp" alt="Example 024">
</div>

---

## Abstract

Smartphone cameras are ubiquitous in daily life, yet their performance can be severely impacted by dirty lenses, leading to degraded image quality. This issue is often overlooked in image restoration research, which assumes ideal or controlled lens conditions. To address this gap, we introduce SIDL (Smartphone Images with Dirty Lenses), a new real-world dataset capturing five types of common contaminants—water droplets, fingerprints, dust, scratches, and mixed debris—paired with clean references across 300 diverse scenes. Each contaminated–clean pair enables supervised learning for robust restoration. We benchmark several state-of-the-art restoration models on SIDL and find that while they partially mitigate blur and occlusion, they struggle with the variety and realism of the degradations. Our results underscore the need for methods tailored to lens contamination. Visit our project site for data, code, and evaluation server.

---

## Image-Acquisition Setup (Figure 2)

<div style="text-align:center;margin:1em 0;">
  <img src="images/image_acquisition_process.gif"
       alt="Custom film-holder and capture pipeline"
       style="max-width:80%;box-shadow:0 0 5px rgba(0,0,0,.2);">
  <p><strong>Figure 2.</strong> A 3D-printed <em>film holder</em> secures PVC “dirty films” directly in front of an iPhone 12 Pro lens. Scenes are captured twice: (b) without a film for a clean reference and (c) with a dirty film to obtain a degraded image. :contentReference[oaicite:2]{index=2}:contentReference[oaicite:3]{index=3}</p>
</div>

---

## SIDL Dataset

SIDL provides 1 ,588 degraded images paired with 300 clean references, covering:

* **Five real degradations**: fingerprint, dust, scratch, water drop, mixed.  
* **Diverse scenes**: indoor/outdoor, day/night, three artificial-light levels.  
* **Difficulty bands**: Easy (PSNR > 25 dB), Medium (20–25 dB), Hard (< 20 dB).  
* **High fidelity**: 4032 × 3024 px ProRAW + full 12-bit DNG release.

### Table 1 – Dataset Comparison

<div style="text-align:center;margin:1em 0;">
  <img src="images/compared.png" alt="Table 1 – Restoration-dataset comparison"
       style="max-width:100%;box-shadow:0 0 5px rgba(0,0,0,.2);">
  <p><strong>Table 1.</strong> Prior dirty-lens datasets are either single-type (Wang et al.) or synthetic (“Let’s see clearly”). SIDL is the first to provide <em>multiple real distortions</em> with paired RAW data at smartphone resolution. :contentReference[oaicite:4]{index=4}:contentReference[oaicite:5]{index=5}</p>
</div>

### Scene Statistics & Difficulty Split

<div style="display:flex;flex-wrap:wrap;gap:1em;margin:1.5em 0;">
  <div style="flex:1;min-width:300px;text-align:center;">
    <img src="images/st.png" alt="Figure 3 – Scene statistics"
         style="max-width:100%;box-shadow:0 0 5px rgba(0,0,0,.2);">
    <p><strong>Figure 3.</strong> 300 scenes span times of day, locations, and light intensities. The train/val/test split is 240 / 20 / 40 scenes. :contentReference[oaicite:6]{index=6}:contentReference[oaicite:7]{index=7}</p>
  </div>
  <div style="flex:1;min-width:300px;text-align:center;">
    <img src="images/figure5.png" alt="Figure 5 – PSNR-based difficulty bands"
         style="max-width:100%;box-shadow:0 0 5px rgba(0,0,0,.2);">
    <p><strong>Figure 5.</strong> PSNR histogram (water-drop example) used to label images as <em>Easy, Medium, Hard</em>. :contentReference[oaicite:8]{index=8}:contentReference[oaicite:9]{index=9}</p>
  </div>
</div>

---

## Benchmark Results

*Six restoration backbones* (AirNet, NAFNet, Restormer, FFTformer, DiffUIR, MambaIR) were trained on SIDL. DiffUIR yields the best PSNR/SSIM across all cases, yet qualitative artifacts remain.

<div style="text-align:center;margin:1em 0;">
  <img src="images/quantitative.png" alt="Table 2 – Quantitative results"
       style="max-width:100%;box-shadow:0 0 5px rgba(0,0,0,.2);">
  <p><strong>Table 2.</strong> PSNR / SSIM (↑) broken down by degradation and difficulty. Best scores in red, second-best in blue. :contentReference[oaicite:10]{index=10}:contentReference[oaicite:11]{index=11}</p>
</div>

<div style="text-align:center;margin:1em 0;">
  <img src="images/qualitative.png" alt="Figure 6 – Qualitative results"
       style="max-width:100%;box-shadow:0 0 5px rgba(0,0,0,.2);">
  <p><strong>Figure 6.</strong> Visual comparison of SotA models on SIDL (medium/hard cases). Persistent halos and color bleeding underscore the challenge. :contentReference[oaicite:12]{index=12}:contentReference[oaicite:13]{index=13}</p>
</div>

---

## Download & Evaluation

### Patchified Images (512 × 512)  
For efficient training and learning, we provide patchified images.

<div class="buttons" style="text-align: center; margin-top: 1em;">
  <a class="button is-primary" href="https://drive.google.com/file/d/1es3rPo5Y9O96EjDVXanUY8NpaRprWH-h/view?usp=sharing" target="_blank">Train Patches</a>
  <a class="button is-primary" href="https://drive.google.com/file/d/1u5-MDauO3XolXsU6eOARwlXo7SnpLwqA/view?usp=sharing" target="_blank">Validation Patches</a>
  <a class="button is-primary" href="https://drive.google.com/file/d/1-SFyyjH0G3C68OfDjZ_O7M4mOqkcJdEf/view?usp=sharing" target="_blank">Test Patches</a>
</div>

### Full-Resolution Images (4032 × 3024)  
High-resolution captures for offline analysis and ISP experiments.

<div class="buttons" style="text-align: center; margin-top: 1em;">
  <a class="button is-primary" href="https://drive.google.com/file/d/1s_gUw1DCqokihl3YtO3lu9_GnLZaSElI/view?usp=sharing" target="_blank">Train Full-Res</a>
  <a class="button is-primary" href="https://drive.google.com/file/d/1OHxG8Jh0goKIhkJTe9NXZ6uIuD5qVaNH/view?usp=sharing" target="_blank">Validation Full-Res</a>
</div>

### RAW Files  
We also provide RAW image files (DNG) along with metadata for ISP-level research.

<div class="buttons" style="text-align: center; margin-top: 1em;">
  <a class="button is-primary" href="https://drive.google.com/file/d/1k78IIsUl2eYPnPvWkBampU0qlMrW4F-u/view?usp=sharing" target="_blank">DNG RAW Images</a>
  <a class="button is-primary" href="https://drive.google.com/file/d/1lAab5F3jjCByY4OEvGSAfykyAqp2wfTi/view?usp=sharing" target="_blank">Metadata (JSON)</a>
</div>

### Online Evaluation  
Click below to evaluate your model on the SIDL benchmark leaderboard.

<div class="buttons" style="text-align: center; margin-top: 1em;">
  <a class="button is-primary" href="http://203.253.25.170:8080" target="_blank">Launch Online Evaluation</a>
</div>

---

## ISP Pipeline  
*(to be released)*

---

## Citation

```bibtex
@inproceedings{choi2025sidl,
  title     = {SIDL: A Real-World Dataset for Restoring Smartphone Images with Dirty Lenses},
  author    = {Choi, Sooyoung and Park, Sungyong and Kim, Heewon},
  booktitle = {Proceedings of the AAAI Conference on Artificial Intelligence},
  volume    = {39}, number = {3}, pages = {2545--2554}, year = {2025}
}
```

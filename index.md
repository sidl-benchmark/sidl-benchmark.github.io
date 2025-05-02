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

> Smartphone cameras are ubiquitous in daily life, yet their performance can be severely impacted by dirty lenses, leading to degraded image quality. This issue is often overlooked in image restoration research, which assumes ideal or controlled lens conditions. To address this gap, we introduce SIDL (Smartphone Images with Dirty Lenses), a new real-world dataset capturing five types of common contaminants—water droplets, fingerprints, dust, scratches, and mixed debris—paired with clean references across 300 diverse scenes. Each contaminated–clean pair enables supervised learning for robust restoration. We benchmark several state-of-the-art restoration models on SIDL and find that while they partially mitigate blur and occlusion, they struggle with the variety and realism of the degradations. Our results underscore the need for methods tailored to lens contamination. Visit our project site for data, code, and evaluation server.

---

## Image Acquisition

We captured each scene using a 3D-printed holder that mounts thin films carrying controlled deposits. By varying the type (e.g., a single water droplet vs. clustered fingerprints), size, and placement of the contaminants, we simulate real-world dirt accumulation on smartphone lenses. The holder ensures precise alignment between contaminated and clean shots.  

<div style="text-align: center; margin: 1em 0;">
  <img src="images/image_acquisition_process.gif" alt="Controlled image acquisition with dirty-lens holder" style="box-shadow: 0 0 5px rgba(0, 0, 0, 0.2); max-width:80%;">
</div>

---

## SIDL Dataset  

SIDL comprises 300 static scenes captured under varied lighting (indoor/outdoor, day/night) and camera settings. For each scene:

- **Clean reference**: an uncontaminated image.  
- **Five degradations**: water, fingerprint, dust, scratch, mixed.  
- **Difficulty levels**: based on reference vs. degraded PSNR, divided into Easy, Medium, and Hard.  

We split scenes into 240 for training, 20 for validation, and 40 for testing.

To illustrate the challenge, SIDL images span a PSNR range from 15 dB (hardest) to 30 dB (easiest) relative to their clean counterparts—far wider than existing benchmarks, which typically assume controlled noise models.

![Dataset comparison chart](images/compared.png)

Our dataset statistics highlight balanced coverage of environment types (e.g., urban, indoor labs) and contaminant appearances.

![Scene distribution across conditions](images/st.png)

---

### Benchmarking Results  

We evaluate several leading restoration methods on SIDL—both classical and deep-learning approaches. While all methods improve perceptual quality and recover fine details under mild blur, their performance degrades sharply on heavy occlusions and nonuniform artifacts. Average PSNR across contaminants ranges from 18 dB (Hard) to 26 dB (Easy), and SSIM from 0.45 to 0.82, leaving substantial room for improvement.

![Quantitative performance plot](images/quantitative.png)

Qualitative examples reveal that common artifacts—such as residual halos around water drops or smearing of fingerprint edges—remain after restoration, especially in complex lighting.

![Sample restoration results on mixed debris](images/qualitative.png)

---

## Download & Evaluation

### Patchified Images (512 × 512)  
Ideal for training batch-based models:

<div class="buttons" style="text-align: center; margin-top: 1em;">
  <a class="button is-primary" href="https://drive.google.com/file/d/1es3rPo5Y9O96EjDVXanUY8NpaRprWH-h/view?usp=sharing" target="_blank">Train Patches</a>
  <a class="button is-primary" href="https://drive.google.com/file/d/1u5-MDauO3XolXsU6eOARwlXo7SnpLwqA/view?usp=sharing" target="_blank">Validation Patches</a>
  <a class="button is-primary" href="https://drive.google.com/file/d/1-SFyyjH0G3C68OfDjZ_O7M4mOqkcJdEf/view?usp=sharing" target="_blank">Test Patches</a>
</div>

### Full-Resolution Images (4032 × 3024)  
For ISP experiments and high-quality restoration:

<div class="buttons" style="text-align: center; margin-top: 1em;">
  <a class="button is-primary" href="https://drive.google.com/file/d/1s_gUw1DCqokihl3YtO3lu9_GnLZaSElI/view?usp=sharing" target="_blank">Train Full-Res</a>
  <a class="button is-primary" href="https://drive.google.com/file/d/1OHxG8Jh0goKIhkJTe9NXZ6uIuD5qVaNH/view?usp=sharing" target="_blank">Validation Full-Res</a>
</div>

### RAW Files & Metadata  
Access DNG files with EXIF and capture settings:

<div class="buttons" style="text-align: center; margin-top: 1em;">
  <a class="button is-primary" href="https://drive.google.com/file/d/1k78IIsUl2eYPnPvWkBampU0qlMrW4F-u/view?usp=sharing" target="_blank">DNG RAW Images</a>
  <a class="button is-primary" href="https://drive.google.com/file/d/1lAab5F3jjCByY4OEvGSAfykyAqp2wfTi/view?usp=sharing" target="_blank">Metadata (JSON)</a>
</div>

### Online Evaluation  
Test your model on our leaderboard server:

<div class="buttons" style="text-align: center; margin-top: 1em;">
  <a class="button is-primary" href="http://203.253.25.170:8080" target="_blank">Launch Evaluation</a>
</div>

---

### ISP Pipeline  
Coming soon.

### Citation

```bibtex
@inproceedings{choi2025sidl,
  title     = {SIDL: A Real-World Dataset for Restoring Smartphone Images with Dirty Lenses},
  author    = {Choi, Sooyoung and Park, Sungyong and Kim, Heewon},
  booktitle = {Proceedings of the AAAI Conference on Artificial Intelligence},
  volume    = {39},
  number    = {3},
  pages     = {2545--2554},
  year      = {2025}
}

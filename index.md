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
data: "https://drive.google.com/drive/folders/1RypnvYYLD3PIld2W4r3NtZQ_SbIDm0w-?usp=sharing"
colab : "https://colab.research.google.com/drive/12sxewePJZcS76chnVguBmKMQKK7XAExP?usp=sharing"
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

Smartphone cameras are ubiquitous in daily life, yet their performance can be severely impacted by dirty lenses, leading to degraded image quality. This issue is often overlooked in image restoration research, which assumes ideal or controlled lens conditions. To address this gap, we introduced SIDL (Smartphone Images with Dirty Lenses), a novel dataset designed to restore images captured through contaminated smartphone lenses. SIDL contains diverse real-world images taken under various lighting conditions and environments. These images feature a wide range of lens contaminants, including water drops, fingerprints, and dust. Each contaminated image is paired with a clean reference image, enabling supervised learning approaches for restoration tasks. To evaluate the challenge posed by SIDL, various state-of-the-art restoration models were trained and compared on this dataset. Their performances achieved some level of restoration but did not adequately address the diverse and realistic nature of the lens contaminants in SIDL. This challenge highlights the need for more robust and adaptable image restoration techniques for restoring images with dirty lenses

---



---

## SIDL Dataset

The SIDL benchmark contains 300 static scenes, each captured twice—once without contamination (clean reference) and once through a thin film carrying a controlled deposit. In total, there are 1,588 degraded–clean image pairs at full ProRAW resolution (4032 × 3024, 12-bit DNG). We simulate five real-world contaminant types—fingerprints, dust, scratches, water drops, and mixed debris—applied to the smartphone lens. To allow fine-grained evaluation, we split the degraded images into three difficulty bands based on PSNR between the clean and dirty images: “Easy”, “Medium”, and “Hard”. Scenes span indoor and outdoor settings, day and night lighting, and three levels of artificial illumination. We allocate 240 scenes for training, 20 for validation, and 40 for testing, ensuring each split has balanced coverage of scene types and difficulty levels.

<div style="text-align:center; margin:1em 0;">
  <img src="images/compared.png" alt="Comparison of SIDL with prior datasets" style="max-width:100%; box-shadow:0 0 5px rgba(0,0,0,.2);">
</div>

SIDL is unique in offering multiple, real distortion types at smartphone resolution, along with paired RAW data and a large, diverse scene set, unlike previous benchmarks that focus on a single distortion or rely on synthetic noise models.

---

## Image Acquisition

To capture perfectly aligned clean and contaminated images, we designed a 3D-printed film holder that mounts directly in front of an iPhone 12 Pro lens. For each scene, we first shoot a clean baseline, then insert a PVC “dirty film” carrying a precise pattern of water, fingerprint oil, dust particles, scratch marks, or a combination thereof, and shoot the degraded version immediately afterward. This procedure guarantees pixel-level correspondence between each clean–dirty pair, while the film holder allows repeatable, controlled placement of contaminants.

<div style="text-align:center; margin:1em 0;">
  <img src="images/image_acquisition_process.gif" alt="Custom film holder pipeline" style="max-width:80%; box-shadow:0 0 5px rgba(0,0,0,.2);">
</div>

---

## Scene Statistics & Difficulty Distribution

The 300 scenes cover a wide variety of environments:

- **Location**: indoor labs, offices, outdoor urban and natural scenes  
- **Time of day**: roughly equal splits of day vs. night  
- **Lighting**: three levels of artificial illumination  

This diversity ensures that models trained on SIDL generalize across realistic conditions. The PSNR values between clean and degraded images range from as low as 12 dB up to over 30 dB, enabling evaluation under mild to severe contamination. By grouping images into Easy, Medium, and Hard bands, researchers can analyze performance trends as contamination severity increases.

<div style="display:flex; flex-wrap:wrap; gap:1em; margin:1.5em 0;">
  <div style="flex:1; min-width:300px; text-align:center;">
    <img src="images/st.png" alt="Scene distribution statistics" style="max-width:100%; box-shadow:0 0 5px rgba(0,0,0,.2);">
  </div>
  <div style="flex:1; min-width:300px; text-align:center;">
    <img src="images/figure5.png" alt="PSNR distribution histogram" style="max-width:100%; box-shadow:0 0 5px rgba(0,0,0,.2);">
  </div>
</div>

---

## Benchmark Results

We evaluated six state-of-the-art restoration architectures (AirNet, NAFNet, Restormer, FFTformer, DiffUIR, and MambaIR) on the SIDL test set. While all models improve perceptual quality under mild contamination, their performance drops notably in the Medium and Hard bands. For example, DiffUIR achieves an average PSNR of 26.3 dB on Easy images but only 18.7 dB on Hard images, with SSIM falling from 0.82 to 0.45. Qualitative examples show persistent halos around water droplets and smearing of fingerprint edges under severe conditions, highlighting the challenge of realistic lens contamination.

<div style="text-align:center; margin:1em 0;">
  <img src="images/quantitative.png" alt="Quantitative PSNR/SSIM results" style="max-width:100%; box-shadow:0 0 5px rgba(0,0,0,.2);">
</div>
<div style="text-align:center; margin:1em 0;">
  <img src="images/qualitative.png" alt="Qualitative restoration examples" style="max-width:100%; box-shadow:0 0 5px rgba(0,0,0,.2);">
</div>

---

## Download & Evaluation

### Patchified Images (512 × 512)  
For efficient batch training, download our pre-cropped patches:

<div class="buttons" style="text-align:center; margin-top:1em;">
  <a class="button is-primary" href="https://drive.google.com/file/d/1es3rPo5Y9O96EjDVXanUY8NpaRprWH-h/view?usp=sharing" target="_blank">Train Patches</a>
  <a class="button is-primary" href="https://drive.google.com/file/d/1u5-MDauO3XolXsU6eOARwlXo7SnpLwqA/view?usp=sharing" target="_blank">Validation Patches</a>
  <a class="button is-primary" href="https://drive.google.com/file/d/1-SFyyjH0G3C68OfDjZ_O7M4mOqkcJdEf/view?usp=sharing" target="_blank">Test Patches</a>
</div>

### Full-Resolution Images (4032 × 3024)  
Download the high-res ProRAW captures for ISP research:

<div class="buttons" style="text-align:center; margin-top:1em;">
  <a class="button is-primary" href="https://drive.google.com/file/d/1s_gUw1DCqokihl3YtO3lu9_GnLZaSElI/view?usp=sharing" target="_blank">Train Full-Res</a>
  <a class="button is-primary" href="https://drive.google.com/file/d/1OHxG8Jh0goKIhkJTe9NXZ6uIuD5qVaNH/view?usp=sharing" target="_blank">Validation Full-Res</a>
</div>

### RAW DNG & Metadata  
Access the original 12-bit DNG files and JSON metadata:

<div class="buttons" style="text-align:center; margin-top:1em;">
  <a class="button is-primary" href="https://drive.google.com/file/d/1k78IIsUl2eYPnPvWkBampU0qlMrW4F-u/view?usp=sharing" target="_blank">DNG RAW Images</a>
  <a class="button is-primary" href="https://drive.google.com/file/d/1lAab5F3jjCByY4OEvGSAfykyAqp2wfTi/view?usp=sharing" target="_blank">Metadata (JSON)</a>
</div>

### Online Evaluation  
Submit your model outputs to our leaderboard server and compare against published baselines:

<div class="buttons" style="text-align:center; margin-top:1em;">
  <a class="button is-primary" href="http://203.253.25.170:8080" target="_blank">Launch Leaderboard</a>
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

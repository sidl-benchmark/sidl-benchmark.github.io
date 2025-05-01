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
/* 1) 화면 전체 폭을 쓰도록 껍데기 컨테이너 폭 풀어주기 */
.gallery-wrapper {
  width: 100vw;
  margin-left: calc((100% - 100vw) / 2);
  display: grid;
  grid-template-columns: repeat(6, 1fr);
  grid-gap: 0;
  padding: 0;
}

/* 2) 이미지 기본, 호버 스타일 */
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

## SIDL Dataset  
We provide 80% of the scenes for training and learning. The remaining scenes are used for online evaluation.

### Patchify images (512×512)  
For efficient training and learning, we provide patchified images.  
<div class="buttons" style="text-align: center; margin-top: 1em;">
  <a class="button is-primary" href="https://drive.google.com/file/d/1es3rPo5Y9O96EjDVXanUY8NpaRprWH-h/view?usp=sharing" target="_blank">Train</a>
  <a class="button is-primary" href="https://drive.google.com/file/d/1u5-MDauO3XolXsU6eOARwlXo7SnpLwqA/view?usp=sharing" target="_blank">Validation</a>
  <a class="button is-primary" href="https://drive.google.com/file/d/1-SFyyjH0G3C68OfDjZ_O7M4mOqkcJdEf/view?usp=sharing" target="_blank">Test</a>
</div>

### Full-resolution images (4032×3024)  
<div class="buttons" style="text-align: center; margin-top: 1em;">
  <a class="button is-primary" href="https://drive.google.com/file/d/1s_gUw1DCqokihl3YtO3lu9_GnLZaSElI/view?usp=sharing" target="_blank">Train</a>
  <a class="button is-primary" href="https://drive.google.com/file/d/1OHxG8Jh0goKIhkJTe9NXZ6uIuD5qVaNH/view?usp=sharing" target="_blank">Validation</a>
</div>

### RAW files  
We also provide RAW image files (DNG) along with metadata.  
<div class="buttons" style="text-align: center; margin-top: 1em;">
  <a class="button is-primary" href="https://drive.google.com/file/d/1k78IIsUl2eYPnPvWkBampU0qlMrW4F-u/view?usp=sharing" target="_blank">DNG images</a>
  <a class="button is-primary" href="https://drive.google.com/file/d/1lAab5F3jjCByY4OEvGSAfykyAqp2wfTi/view?usp=sharing" target="_blank">Metadata</a>
</div>

### Online Evaluation  
<div class="buttons" style="text-align: center; margin-top: 1em;">
  <a class="button is-primary" href="http://203.253.25.170:8080" target="_blank">Click here to launch evaluation</a>
</div>

Click the button above to evaluate your model on the SIDL benchmark.

### ISP pipeline  
Coming soon

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

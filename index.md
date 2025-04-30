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
paper: "https://ojs.aaai.org/index.php/AAAI/article/view/32257"
video: "https://youtu.be/5nSJh-IPWd0"
code: "https://github.com/sidl-benchmark/sidl-benchmark.github.io"
data: "https://github.com/your-repo/dataset"
---

<!-- 페이지 전역 스타일 (이 페이지에서만 적용) -->
<style>
.gallery-wrapper .image img {
  width: 100%;
  transition: width 0.3s ease;
}
.gallery-wrapper .image img:hover {
  position: relative;
  width: 1064px !important;
  z-index: 10;
}
</style>

<hr>

<div class="gallery-wrapper">
  <div class="columns is-multiline">

    <div class="column is-2"><figure class="image"><img src="images/Web_01_W.png" alt="Example 001"></figure></div>
    <div class="column is-2"><figure class="image"><img src="images/Web_02_D.png" alt="Example 002"></figure></div>
    <div class="column is-2"><figure class="image"><img src="images/Web_03_F.jpg" alt="Example 003"></figure></div>
    <div class="column is-2"><figure class="image"><img src="images/Web_04_W.png" alt="Example 004"></figure></div>
    <div class="column is-2"><figure class="image"><img src="images/Web_05_F.png" alt="Example 005"></figure></div>
    <div class="column is-2"><figure class="image"><img src="images/Web_06_W.png" alt="Example 006"></figure></div>

    <div class="column is-2"><figure class="image"><img src="images/Web_07_W.png" alt="Example 007"></figure></div>
    <div class="column is-2"><figure class="image"><img src="images/Web_08_S.png" alt="Example 008"></figure></div>
    <div class="column is-2"><figure class="image"><img src="images/Web_09_W.jpg" alt="Example 009"></figure></div>
    <div class="column is-2"><figure class="image"><img src="images/Web_10_W.jpg" alt="Example 010"></figure></div>
    <div class="column is-2"><figure class="image"><img src="images/Web_11_W.png" alt="Example 011"></figure></div>
    <div class="column is-2"><figure class="image"><img src="images/Web_12_S.png" alt="Example 012"></figure></div>

    <div class="column is-2"><figure class="image"><img src="images/Web_13_F.png" alt="Example 013"></figure></div>
    <div class="column is-2"><figure class="image"><img src="images/Web_14_W.jpg" alt="Example 014"></figure></div>
    <div class="column is-2"><figure class="image"><img src="images/Web_15_F.jpg" alt="Example 015"></figure></div>
    <div class="column is-2"><figure class="image"><img src="images/Web_16_S.png" alt="Example 016"></figure></div>
    <div class="column is-2"><figure class="image"><img src="images/Web_17_S.jpg" alt="Example 017"></figure></div>
    <div class="column is-2"><figure class="image"><img src="images/Web_18_F.jpg" alt="Example 018"></figure></div>

    <div class="column is-2"><figure class="image"><img src="images/Web_19_D.jpg" alt="Example 019"></figure></div>
    <div class="column is-2"><figure class="image"><img src="images/Web_20_F.png" alt="Example 020"></figure></div>
    <div class="column is-2"><figure class="image"><img src="images/Web_21_D.jpg" alt="Example 021"></figure></div>
    <div class="column is-2"><figure class="image"><img src="images/Web_22_W.jpg" alt="Example 022"></figure></div>
    <div class="column is-2"><figure class="image"><img src="images/Web_23_F.jpg" alt="Example 023"></figure></div>
    <div class="column is-2"><figure class="image"><img src="images/Web_24_W.png" alt="Example 024"></figure></div>

  </div>
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

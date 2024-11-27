---
title: Towards a malware family classification model using static call graph instruction visualization
layout: default
---

<link rel="stylesheet" href="../../style.css" />

<script type="text/javascript" src="https://cdn.jsdelivr.net/gh/pcooksey/bibtex-js@1.0.0/src/bibtex_js.min.js"></script>

<link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/4.0.0/css/bootstrap.min.css" integrity="sha384-Gn5384xqQ1aoWXA+058RXPxPg6fy4IWvTNh0E263XmFcJlSAwiGgFAW/dAiS6JXm" crossorigin="anonymous">
<script src="https://maxcdn.bootstrapcdn.com/bootstrap/4.0.0/js/bootstrap.min.js" integrity="sha384-JZR6Spejh4U02d8jOt6vLEHfe/JQGiRRSQQxSfFWpi1MquVdAyjUar5+76PVCmYl" crossorigin="anonymous"></script>

### About

* presented at <a href="https://nsclab.org/nss-socialsec2024/" target="blank">NSS 2024</a>
* <a href="./nss.pdf" target="_blank">slides</a>

### Authors

* <a href="https://www.researchgate.net/profile/Zalan-Bodo">Zalán Bodó</a>
* <a href="https://www.researchgate.net/profile/P-Vinod">Vinod P. </a>
* <a href="https://www.researchgate.net/profile/Mauro-Conti">Mauro Conti</a>
* <a href="https://www.researchgate.net/profile/Attila-Mester-2">Attila Mester </a>

### Abstract

<div class="inner" style="font-style: italic">
    <span class="apostrophe apostrophe-l">"</span>
This paper offers yet another static analysis method aimed
at classifying malware families, by disassembling the executables with
Radare2 and traversing the static call graph to train CNNs on
instruction-based RGB images. The instruction-based family detection
should have the potential to model common behavioral patterns, thus
creating a profile for various families and actors. The experiments are
carried out on the BODMAS, MalImg, and IBD (internal Bitdefender
dataset). Our method’s performance is compared to another static fea-
ture selection method – the EMBER features. Furthermore, we reveal
proof of correlation between packers and malware families in all three
datasets. Our conclusion states that the proposed model’s accuracy does
not reach the EMBER feature’s performance due to the high number
of packed files in these datasets. However, its stability still motivates
its use since the instruction-based information cannot be altered easily
as header-based features – our observations infer that while classifying
malware families, ML methods which ignore unpacking the samples may
overfit the data, learning packer traits instead of actual family behaviour,
offering no explainability over the decision.
    <span class="apostrophe apostrophe-r">"</span>
</div>

### Keywords

<div class="inner" style="padding-bottom: 0"></div>

`static malware analysis`<span class="apostrophe">,</span>
`call graph`<span class="apostrophe">,</span>
`control flow graph`<span class="apostrophe">,</span>
`Radare2`<span class="apostrophe">,</span>
`family classification`<span class="apostrophe">,</span>
`packer`<span class="apostrophe">,</span>
`BODMAS`<span class="apostrophe">,</span>
`EMBER`<span class="apostrophe">,</span>
`MalImg`


<div class="inner" style="padding-top: 0"></div>

### Dataset

* published on Kaggle: [https://www.kaggle.com/datasets/amester/malflow](https://www.kaggle.com/datasets/amester/malflow)
---
title: Towards a malware family classification model using static call graph instruction visualization
layout: default
---

<link rel="stylesheet" href="../../style.css" />

<script src="https://code.jquery.com/jquery-3.2.1.min.js"></script>
<script type="text/javascript" src="https://cdn.jsdelivr.net/gh/pcooksey/bibtex-js@1.0.0/src/bibtex_js.min.js"></script>

<link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/4.0.0/css/bootstrap.min.css" integrity="sha384-Gn5384xqQ1aoWXA+058RXPxPg6fy4IWvTNh0E263XmFcJlSAwiGgFAW/dAiS6JXm" crossorigin="anonymous">
<script src="https://maxcdn.bootstrapcdn.com/bootstrap/4.0.0/js/bootstrap.min.js" integrity="sha384-JZR6Spejh4U02d8jOt6vLEHfe/JQGiRRSQQxSfFWpi1MquVdAyjUar5+76PVCmYl" crossorigin="anonymous"></script>

<script src="https://cdnjs.cloudflare.com/ajax/libs/ekko-lightbox/5.3.0/ekko-lightbox.min.js" integrity="sha512-Y2IiVZeaBwXG1wSV7f13plqlmFOx8MdjuHyYFVoYzhyRr3nH/NMDjTBSswijzADdNzMyWNetbLMfOpIPl6Cv9g==" crossorigin="anonymous"></script>
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/ekko-lightbox/5.3.0/ekko-lightbox.css" integrity="sha512-Velp0ebMKjcd9RiCoaHhLXkR1sFoCCWXNp6w4zj1hfMifYB5441C+sKeBl/T/Ka6NjBiRfBBQRaQq65ekYz3UQ==" crossorigin="anonymous" />

<script>
    $().ready(function() {
        $("[data-custom-image]").each(function() {             
            let $img = $("<img class='img-fluid gallery'/>");
            $img.attr({
                src: $(this).data('src')
            });

            let $a = $("<a data-toggle='lightbox' />");
            $a.attr({
                href: $(this).data('src')
            });
            
            ["title", "footer", "gallery"].map(key => {
                if (key in $(this).data()) {
                    $a.data(key, $(this).data(key));
                }
            })
            
            $a.append($img);
            $(this).prepend($a);
        });

        $(document).on('click', '[data-toggle="lightbox"]', function(event) {
            event.preventDefault();
            $(this).ekkoLightbox({
                loadingMessage: "",
                leftArrow: "<span style='color:darkgrey'>❮</span>",
                rightArrow: "<span style='color:darkgrey'>❯</span>"
            });
        });
    });
</script>


### About

* Presented at <a href="https://nsclab.org/nss-socialsec2024/" target="blank">NSS 2024</a>
* <a href="./nss.pdf" target="_blank">Slides</a>
* GitHub repository: <a href="https://github.com/attilamester/malflow" target="_blank">malflow</a>

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


### Figures

<div class="inner" data-custom-image data-src="img/flow.png">
    <div class="caption">
        <span class="caption">Fig. 1.</span>Outline of the project: static call graph instruction image generation and family classification using CNNs
    </div>
</div>

<div class="inner row">
    <div class="col-md-6">
    <a data-toggle="lightbox" href="img/ainslot.png" data-gallery="g">
        <img src="img/ainslot.png" class="img-fluid gallery" /></a>
    </div>
    <div class="col-md-6">
    <a data-toggle="lightbox" href="img/ainslot_2.png" data-gallery="g">
        <img src="img/ainslot_2.png" class="img-fluid gallery" /></a>
    </div>
    
    <div class="caption">
        <span class="caption">Fig. 2.</span>Two samples from <b>ainslot</b> family, visualized by encoding their static call graph instructions 
    </div>
</div>

<div class="inner row">
    <div class="col-md-6">
    <a data-toggle="lightbox" href="img/allaple_1.png" data-gallery="g">
        <img src="img/allaple_1.png" class="img-fluid gallery" /></a>
    </div>
    <div class="col-md-6">
    <a data-toggle="lightbox" href="img/allaple_2.png" data-gallery="g">
        <img src="img/allaple_2.png" class="img-fluid gallery" /></a>
    </div>
    
    <div class="caption">
        <span class="caption">Fig. 3.</span>Two samples from <b>allaple</b> family, visualized by encoding their static call graph instructions 
    </div>
</div>
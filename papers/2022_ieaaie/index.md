---
title: Malware classification based on graph convolutional neural networks and static call graph features
layout: default
filename: ieaaie2022.md
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

* Presented at <a href="https://ieaaie2022.wordpress.com/" target="blank">IEA/AIE 2022</a>
* <a href="./ieaaie2022.pdf" target="_blank">Slides</a>

### Authors

* <a href="https://www.researchgate.net/profile/Zalan-Bodo">Zalán Bodó</a>
* <a href="https://www.researchgate.net/profile/Attila-Mester-2">Attila Mester </a>

### Abstract

<div class="inner" style="font-style: italic">
    <span class="apostrophe apostrophe-l">"</span>

Advanced Persistent Threats (APT) are targeted, high level
cybersecurity risk factors facing governments, financial units and other
organizations. The attribution of APTs - gathering information about
the origin of an attack - is an important key in the process of securing
an organisation’s infrastructure, prioritizing the measures to be taken
depending on the actor(s) targeting the organisation. In practice, an elementary step in the process of attribution is determining the family
and/or author of a sample, based on the binary file and/or its dynamic
analysis - i.e. a multi-class classification problem regarding the family/author label. There are numerous methods in the literature aimed to
label a sample based on its control flow graph or API sequence graph.
We aim to summarize the literature on these methods, and offer another
method to classify malware families leveraging the static call graph of a
PE executable, as well as the functions’ instruction lists, using a locality-
sensitive hashing method to obtain the node feature vectors. Our results
are compared to recent publications in the field.

<span class="apostrophe apostrophe-r">"</span>
</div>

### Keywords

<div class="inner" style="padding-bottom: 0"></div>

`static malware analysis`<span class="apostrophe">,</span>
`static call graph`<span class="apostrophe">,</span>
`graph convolutional neural networks`<span class="apostrophe">,</span>
`locality-sensitive hashing`<span class="apostrophe">,</span>
`family classification`

<div class="inner" style="padding-top: 0"></div>


### Figures

<div class="inner" data-custom-image data-src="img/gcn_flow.png">
    <div class="caption">
        <span class="caption">Fig. 1.</span>Outline of the project: malware family classification using graph convolutional neural networks trained on static call graph
    </div>
</div>

<div class="inner row">
    <div class="col-md-6">
    <a data-toggle="lightbox" href="img/cg-nodes.png" data-gallery="g">
        <img src="img/cg-nodes.png" class="img-fluid gallery" /></a>
    </div>
    <div class="col-md-6">
    <a data-toggle="lightbox" href="img/cg-edges.png" data-gallery="g">
        <img src="img/cg-edges.png" class="img-fluid gallery" /></a>
    </div>
    
    <div class="caption">
        <span class="caption">Fig. 2.</span>Histogram of number of nodes and edges in a call graph. 
    </div>
</div>
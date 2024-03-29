---
layout: default
title: Validating static call graph-based malware signatures using community detection methods
---

<script src="https://code.jquery.com/jquery-3.2.1.min.js"></script>
<script type="text/javascript" src="https://cdn.jsdelivr.net/gh/pcooksey/bibtex-js@1.0.0/src/bibtex_js.min.js"></script>
<!--
<script src="https://cdn.jsdelivr.net/npm/js-image-zoom/js-image-zoom.min.js"></script>
-->

<link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/4.0.0/css/bootstrap.min.css" integrity="sha384-Gn5384xqQ1aoWXA+058RXPxPg6fy4IWvTNh0E263XmFcJlSAwiGgFAW/dAiS6JXm" crossorigin="anonymous">
<script src="https://maxcdn.bootstrapcdn.com/bootstrap/4.0.0/js/bootstrap.min.js" integrity="sha384-JZR6Spejh4U02d8jOt6vLEHfe/JQGiRRSQQxSfFWpi1MquVdAyjUar5+76PVCmYl" crossorigin="anonymous"></script>

<script src="https://cdnjs.cloudflare.com/ajax/libs/ekko-lightbox/5.3.0/ekko-lightbox.min.js" integrity="sha512-Y2IiVZeaBwXG1wSV7f13plqlmFOx8MdjuHyYFVoYzhyRr3nH/NMDjTBSswijzADdNzMyWNetbLMfOpIPl6Cv9g==" crossorigin="anonymous"></script>
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/ekko-lightbox/5.3.0/ekko-lightbox.css" integrity="sha512-Velp0ebMKjcd9RiCoaHhLXkR1sFoCCWXNp6w4zj1hfMifYB5441C+sKeBl/T/Ka6NjBiRfBBQRaQq65ekYz3UQ==" crossorigin="anonymous" />

<link rel="stylesheet" href="../../style.css" />

<script>
    $().ready(function() {
        let $container = $("<div id='logo_container'></div>");
        let $logo = $("<img id='logo'/>");
        $logo.attr({
            "src": "./img/teaserfigure.png",
            "alt": "Malware community graph",
        });
        $container.append($logo);
        $("div#header_wrap").css("position", "relative").append($container);

        //$("img").each(function() {
        //    return;
        //    if ($(this).attr("id") == "logo") {
        //        return;
        //    }
        //    new ImageZoom($(this).parent()[0], {width: 500, zoomWidth: 500, zoomPosition: "top"});
        //});

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

* Presented at <a href="https://www.esann.org/" target="blank">ESANN 2021</a>
* Authors:
    * Zalán Bodó
    * Attila Mester (supervisor: Anca-Mirela Andreica)
* <a href="./img/poster.png" target="_blank">Poster spotlight</a>
  
### Abstract

<div class="inner" style="font-style: italic">
    <span class="apostrophe apostrophe-l">"</span>
    Due to the increasing number of new malware appearing
daily, it is impossible to manually inspect each sample. By applying data
mining techniques to analyze the program code, we can help manual processing. In this paper we propose a method to extract signatures from the
executable binary of a malware, in order to query the local neighborhood
in real time. The method is validated by applying community detection
algorithms on the common fingerprints-based malware graph to identify
families, and assessing these with evaluation metrics used in the field (e.g.
modularity, family majority, etc.). The signatures are obtained via static
code analysis, using function call n-grams and applying locality-sensitive
hashing techniques to enable the match between functions with highly
similar instruction lists.
    <span class="apostrophe apostrophe-r">"</span>

</div>

### Keywords

<div class="inner" style="padding-bottom: 0"></div>

`static call graph`<span class="apostrophe">,</span>
`n-gram features`<span class="apostrophe">,</span>
`locality-sensitive hashing`<span class="apostrophe">,</span>
`malware communities`<span class="apostrophe">,</span> 
`family clustering`

<div class="inner" style="padding-top: 0"></div>

### Related work

<div class="inner" data-custom-image data-src="img/research_papers_2.png">
    <div class="caption">
        <span class="caption">Fig. 1.</span>Prevalent methods and feautures used for malware analysis 
        (based on <a href="#cite_1"><span class="cite">[1]</span></a>)
    </div>
</div>

<div class="inner" data-custom-image data-src="img/research_papers_call_graph.png">
    <div class="caption">
        <span class="caption">Fig. 2.</span>Call graph-based malware analysis
        (based on <a href="#cite_1"><span class="cite">[1]</span></a>)
    </div>
</div>

### Figures

<div class="inner" data-custom-image data-src="img/teaserfigure.png">
    <div class="caption">
        <span class="caption">Fig. 3.</span>Louvain communities of the common fingerprints-based malware graph
    </div>
</div>



<div class="inner row">
    <div class="col-md-6">
    <a data-toggle="lightbox" href="img/a_color.png" data-gallery="g" data-title="Sample <b>s1</b>, having ~7600 signatures" data-footer="<div>~380 DLL <b>|</b> ~2800 lib. functions <b>|</b> ~800 subroutines</div>">
        <img src="img/a_color.png" class="img-fluid gallery" /></a>
    </div>
    <div class="col-md-6">
    <a data-toggle="lightbox" href="img/b_color.png" data-gallery="g" data-title="Sample <b>s2</b>, having ~6900 signatures" data-footer="<div>Same DLL functions <b>|</b> ~2500 lib. functions (<em>~2300</em> identical with <b>s1</b>) <b>|</b> ~750 subroutines (<em>~730</em> identical with <b>s1</b>)</div>">
        <img src="img/b_color.png" class="img-fluid gallery" /></a>
    </div>
    
    <div class="caption">
        <span class="caption">Fig. 4.</span>Call graphs of two samples within the same community, having the same family, and <b>~4800</b> common signatures 
    </div>
</div>



<bibtex src="bib.bib"></bibtex>

<div class="bibtex_template"> 
    <div style="display: flex; margin-bottom: 5px">
        <div style="margin-right: 10px; font-family: consolas">
            [<span class="bibtexVar" extra="BIBTEXKEY" id="cite_+BIBTEXKEY+"><span class="bibtexkey"></span></span>]
        </div>
        <div>
            <div style="font-weight: bold;">
                <span class="if year">
                    <span class="year"></span>, 
                </span>
                
                <span class="if type">
                    <span class="type"></span>,
                </span>
                
                <span class="author"></span>

                <span class="if url" style="margin-left: 20px">
                    <a class="url" style="color:black; font-size:10px" target="_blank">(view)</a>
                </span>
                
                <span class="if !url"> 
                <span class="if doi">
                    <a class="bibtexVar" style="color:black; font-size:10px" target="_blank" href="https://www.doi.org/+doi+" extra="doi">(view)</a>
                </span>
                </span>
                
            </div>
            <div>
                <span class="title"></span>
            </div>
        </div>
    </div>
</div>

### References

<div class="inner" style="max-height: 500px; overflow: auto">
    <div id="bibtex_display"></div>
</div>
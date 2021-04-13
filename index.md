---
layout: default
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

<style>
    div.inner {
        padding: 20px 0px;
    }

    #logo {
        height: 100%; 
        border: none; 
        box-shadow: none;
        margin: 0;
    }
    #logo_container {
        position: absolute; 
        top: 0; 
        right: 30px; 
        bottom: 0; 
        margin: auto; 
        height: 60%;
    }
    @media only screen and (max-width: 1000px) {
        #logo_container {
            display: none;
        }
    }

    span.cite {
        font-family: consolas;
    }

    span.apostrophe {
        color: darkgray;
        font-weight: bold;
        font-size: 1.5em;
        line-height: 1em;
        display: inline-block;
    }

    span.apostrophe-l {
        margin-right: 10px;
    }
    
    span.apostrophe-r {
        margin-left: 10px;
    }

    div.caption {
        text-align: center;
        margin-bottom: 15px;
    }

    div.caption::before {
        color: darkgray;
        content: '•';
        font-weight: bold;
        font-size: 1.5em;
        display: inline-block;
        margin-right: 5px;
    }
    
    span.caption {
        font-weight: bold;
        color: darkgrey;
        margin-right: 10px;
    }
    
    img.gallery {
        width: 100%;
        border: none;
        box-shadow: none;
    }
</style>
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


### Abstract

<div class="inner" style="font-style: italic">
    <span class="apostrophe apostrophe-l">"</span>
    Due to the increasing number of new malware appearing daily, it is impossible to manually inspect each sample. By applying data mining techniques to detect malicious programs, we can help manual analysis, based on static as well as dynamic features. In this paper we propose a method to extract fingerprints from the executable binary, and evaluate these by applying community detection algorithms on the common fingerprints-based malware graph to identify families. The signatures are extracted via static code analysis, using n-grams obtained from the function call graph and applying locality-sensitive hashing to catch slight variations of the instruction sequences.
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
    <a data-toggle="lightbox" href="img/a.png" data-gallery="g">
        <img src="img/a.png" class="img-fluid gallery" /></a>
    </div>
    <div class="col-md-6">
    <a data-toggle="lightbox" href="img/b.png" data-gallery="g">
        <img src="img/b.png" class="img-fluid gallery" /></a>
    </div>
    
    <div class="caption">
        <span class="caption">Fig. 4.</span>Call graphs of two samples within the same community, having the same family
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
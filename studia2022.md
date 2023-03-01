---
title: Malware analysis and static call graph generation with Radare2
layout: default
filename: studia2022.md
---

<link rel="stylesheet" href="./style.css" />

<script type="text/javascript" src="https://cdn.jsdelivr.net/gh/pcooksey/bibtex-js@1.0.0/src/bibtex_js.min.js"></script>

<link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/4.0.0/css/bootstrap.min.css" integrity="sha384-Gn5384xqQ1aoWXA+058RXPxPg6fy4IWvTNh0E263XmFcJlSAwiGgFAW/dAiS6JXm" crossorigin="anonymous">
<script src="https://maxcdn.bootstrapcdn.com/bootstrap/4.0.0/js/bootstrap.min.js" integrity="sha384-JZR6Spejh4U02d8jOt6vLEHfe/JQGiRRSQQxSfFWpi1MquVdAyjUar5+76PVCmYl" crossorigin="anonymous"></script>

### About

* submitted to <a href="http://www.cs.ubbcluj.ro/~studia-i/journal/journal" target="blank">Studia Universitatis Babeș-Bolyai Informatica 2022</a>

### Abstract

<div class="inner" style="font-style: italic">
    <span class="apostrophe apostrophe-l">"</span>

A powerful feature used in automated malware analysis is the static call graph of the executable file. 
Elimination of sandbox environment, fast scan, function call patterns beyond instruction level information -- 
all of these motivate the prevalence of the feature. Processing and storing the static call graph of 
malicious samples in a scaled manner facilitates the application of complex network analysis in malware research. 
IDA Pro is one of the leading disassembler tools in the industry <a href="#cite_1"><span class="cite">[1]</span></a>, <a href="#cite_2"><span class="cite">[2]</span></a> which offers the generation 
of the call graph via `GenCallGdl` and `GenFuncGdl` APIs -- a tool which we used in our 
previous works <a href="#cite_3"><span class="cite">[3]</span></a>, <a href="#cite_4"><span class="cite">[4]</span></a>}.
In this paper we offer an alternative analysis using another disassembler tool, <a href="https://github.com/radareorg/radare2" target="_blank">Radare2</a>, 
an open-source Unix-based software, which is also frequently used in this 
domain 
<a href="#cite_5"><span class="cite">[5]</span></a>,
<a href="#cite_6"><span class="cite">[6]</span></a>, 
<a href="#cite_7"><span class="cite">[7]</span></a>, 
<a href="#cite_8"><span class="cite">[8]</span></a>, 
<a href="#cite_9"><span class="cite">[9]</span></a>. 
Radare2 has Python support (among other languages), via the `r2pipe` package, thus enabling 
full scalability on Linux-based servers using containerized solutions. 
This paper offers a detailed technical description on how to use Radare2 to generate 
the static call graph of a PE file and a thorough comparison with 
the output of IDA Pro, as well as a public dataset on which the experiments were carried out.

    <span class="apostrophe apostrophe-r">"</span>
</div>

### Keywords

<div class="inner" style="padding-bottom: 0"></div>

`static call graph`<span class="apostrophe">,</span>
`IDA Pro 6`<span class="apostrophe">,</span>
`Radare2`<span class="apostrophe">,</span>
`Levensthein`<span class="apostrophe">,</span>
`Jaro`<span class="apostrophe">,</span>
`Jaccard`

<div class="inner" style="padding-top: 0"></div>

### Dataset

* selection from <a href="https://www.kaggle.com/competitions/malware-detection/data" target="_black">Kaggle</a>
* <a href="./studia2022_md5s.txt" target="_blank">selected dataset</a>


<bibtex src="studia2022.bib"></bibtex>

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
---
layout: default
title: Research work on malware analyis
home: true
subtitle:
    <br/>
    Authors
    <ul>
        <li>
            Attila Mester 
                <a href="https://www.linkedin.com/in/attilamester/"><img src="https://static.licdn.com/sc/h/akt4ae504epesldzj74dzred8" /></a>
                <a href="https://www.researchgate.net/profile/Attila-Mester-2"><img src="https://c5.rgstatic.net/m/41542880220916/images/favicon/favicon-32x32.png" /></a>
        </li>
        <li>
            dr. Zalán Bodó 
                <a href="http://www.cs.ubbcluj.ro/~zbodo"><img src="https://www.ubbcluj.ro/template/favicon-32x32.png" /></a>                
                <a href="https://www.linkedin.com/in/zal%C3%A1n-bod%C3%B3-66b915b9/"><img src="https://static.licdn.com/sc/h/akt4ae504epesldzj74dzred8" /></a>
                <a href="https://www.researchgate.net/profile/Zalan-Bodo"><img src="https://c5.rgstatic.net/m/41542880220916/images/favicon/favicon-32x32.png" /></a>
        </li>
    </ul>
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

<link rel="stylesheet" href="./style.css" />
<style>
#project_title {
font-size: 2em;
}
#project_subtitle {
font-size: 1.5em;
}

#main_content_wrap > section {
    max-width: 900px;
}

.card-container {
    display: flex;
    align-items: flex-start;
    flex-wrap: wrap;
}
@media (max-width: 600px) {
    .card-container {
        flex-direction: column;
    }
    .card {
        width: 100% !important;
        margin: 8px 0px !important;
    }
}

.card {
    position: relative;
    width: 250px;
    margin: 8px;
}

.card img {
    box-shadow: none;
}

.card .card-title {
    font-weight: bold;
}

.card-highlight {
    position: absolute;
    top: -5px;
    right: -5px;
}

.card-highlight > span {
    background: #9c9cf3;
    color: white;
    padding: 5px 10px;
    border-radius: 5px;
}

</style>

<div class="card-container">

<div class="card">
  <img class="card-img-top" src="./papers/2021_esann/img/teaserfigure.png" alt="Card image cap">
  <div class="card-body">
    <h5 class="card-title">Validating static call graph-based malware signatures using community detection methods</h5>
    <p class="card-text">ESANN, 2021</p>
    <a href="papers/2021_esann" class="btn btn-primary">View</a>
  </div>
</div>

<div class="card">
  <img class="card-img-top" src="./papers/2022_ieaaie/img/GCN-LSH.png" alt="Card image cap">
  <div class="card-body">
    <h5 class="card-title">Malware classification based on graph convolutional neural networks and static call graph features</h5>
    <p class="card-text">IEA/AIE, 2022</p>
    <a href="papers/2022_ieaaie" class="btn btn-primary">View</a>
  </div>
</div>

<div class="card">
  <img class="card-img-top" src="./papers/2022_studia/img/r2.png" alt="Card image cap">
  <div class="card-body">
    <h5 class="card-title">Malware analysis and static call graph generation with Radare2</h5>
    <p class="card-text" style="color:grey; font-style: italic">
        # peer review: accepted <br/>
        # publication pending
    </p>
    <p class="card-highlight">
        <span>Latest work</span>
    </p>
    <a href="papers/2022_studia" class="btn btn-primary">View</a>
  </div>
</div>


</div>

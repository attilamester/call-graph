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
<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/bootstrap-icons@1.5.0/font/bootstrap-icons.css">
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
    max-width: 1090px;
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
    margin: 0;
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
    <p class="card-text"><a href="https://www.esann.org/esann21programme" target="blank">ESANN, 2021</a></p>
    <a href="papers/2021_esann" class="btn btn-primary">View</a>
    <a href="https://www.esann.org/sites/default/files/proceedings/2021/ES2021-27.pdf" target="blank"><i class="bi bi-paperclip"></i>Paper</a>
  </div>
</div>

<div class="card">
  <img class="card-img-top" src="./papers/2022_ieaaie/img/gcn_flow.png" alt="Card image cap">
  <div class="card-body">
    <h5 class="card-title">Malware classification based on graph convolutional neural networks and static call graph features</h5>
    <p class="card-text"><a href="https://ieaaie2022.wordpress.com/" target="blank">IEA/AIE, 2022</a></p>
    <a href="papers/2022_ieaaie" class="btn btn-primary">View</a>
    <a href="https://link.springer.com/chapter/10.1007/978-3-031-08530-7_45" target="blank"><i class="bi bi-paperclip"></i>Paper</a>
  </div>
</div>

<div class="card">
  <img class="card-img-top" src="./papers/2022_studia/img/r2.png" alt="Card image cap">
  <div class="card-body">
    <h5 class="card-title">Malware analysis and static call graph generation with Radare2</h5>
    <p class="card-text">
        <a href="https://www.cs.ubbcluj.ro/~studia-i/journal/journal/article/view/85" target="blank">
        Studia Universitatis Informatica, 2023
        </a>
    </p>
    
    <a href="papers/2022_studia" class="btn btn-primary">View</a>
    <a href="https://www.cs.ubbcluj.ro/~studia-i/journal/journal/article/view/85/85" target="blank"><i class="bi bi-paperclip"></i>Paper</a>
    <a href="https://www.kaggle.com/competitions/malware-detection/data" target="_blank" class="btn">
        <i class="bi bi-file-earmark-fill"></i>
        Kaggle dataset
    </a>
  </div>
</div>

<div class="card">
<div style="display: flex">
<div>
  <img class="card-img-top" src="./papers/2024_nss/img/ainslot.png" alt="Card image cap">
  <img class="card-img-top" src="./papers/2024_nss/img/ainslot_gray.png" alt="Card image cap">
</div>
<div>
  <img class="card-img-top" src="./papers/2024_nss/img/ainslot_pe1.png" alt="Card image cap">
  <img class="card-img-top" src="./papers/2024_nss/img/ainslot_pe2.png" alt="Card image cap">
</div>
</div>

  <div class="card-body">
    <h5 class="card-title">Towards a malware family classification model
using static call graph instruction visualization</h5>
    <p class="card-text">
        <a href="https://nsclab.org/nss-socialsec2024/papers.html" target="blank">
        NSS, 2024
        </a>
    </p>
    <p class="card-highlight">
        <span>Latest work</span>
    </p>
    <a href="papers/2024_nss" class="btn btn-primary">View</a>
    <a href="https://link.springer.com/chapter/10.1007/978-981-96-3531-3_9" target="blank"><i class="bi bi-paperclip"></i>Paper</a>
    <div>
    <a href="https://github.com/attilamester/malflow" target="_blank" class="btn"><i class="bi bi-github"></i>
        malflow
    </a>
    <a href="https://www.kaggle.com/datasets/amester/malflow" target="_blank" class="btn">
        <i class="bi bi-file-earmark-fill"></i>
        Kaggle dataset
    </a>
    </div>
  </div>
</div>

</div>


<h3>Other</h3>

<div class="card-container">


<div class="card">
  <img class="card-img-top" src="./papers/2021_mdpi/img/fb-pol-louvain.png" alt="Card image cap" height="160">
  <div class="card-body">
    <h5 class="card-title">Network Analysis Based on Important Node Selection and Community Detection</h5>
    <p class="card-text">
         <a href="https://www.mdpi.com/2227-7390/9/18/2294" target="blank">
        MDPI Mathematics, 2021
        </a>
    </p>
    <a href="https://www.mdpi.com/2227-7390/9/18/2294" target="blank"><i class="bi bi-paperclip"></i>Paper</a>
  </div>
</div>

<div class="card">
  <div style="overflow: hidden; margin: 5px;">
  <img class="card-img-top" src="https://www.2022.itdays.ro/images/imgs7_2022.png" alt="Card image cap" height="160"
    style="object-fit: cover; object-position: 4% -22px; scale: 1.5;">   
  </div>

  <div class="card-body">
    <h5 class="card-title">IT Days 2022</h5>
    <a href="https://www.2022.itdays.ro/presentation/Research-and-Academic-Initiatives-in-Cyber-Security-at-Babe%C8%99-Bolyai-University" target="blank"><i class="bi bi-paperclip"></i>Speaker</a>
  </div>
</div>

<!--
<div class="card">
  <img class="card-img-top" src="./assets/images/phd_cover.png" alt="Card image cap" height="160">
  <div class="card-body">
    <h5 class="card-title">PhD defense 2025</h5>
  </div>
</div>
-->



</div>

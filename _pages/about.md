---
layout: page
permalink: /
title: about
nav: about
description: <a href="http://www.ml.cmu.edu/" class="page-description" target="_blank">Machine Learning Department</a> • <a href="http://www.cs.cmu.edu/" class="page-description" target="_blank">School of Computer Science</a> • <a href="http://www.cmu.edu/" class="page-description" target="_blank">Carnegie Mellon University</a>
address: <a href="https://www.google.com/maps/place/Gates+Center+for+Computer+Science/@40.4432641,-79.9449469,19.18z/data=!4m5!3m4!1s0x8834f22175d2f3cf:0x963e80aba7fde2d0!8m2!3d40.4435476!4d-79.9446184" class="page-description" target="_blank">8227 Gates Hillman Center, 5000 Forbes Ave, Pittsburgh, PA 15213</a>
---

<div class="col p-0 pt-4 pb-4">
  <h1 class="pb-3 title text-left font-weight-bold">Otilia Stretcu</h1>
  <h6 class="m-0 mb-2" style="font-size: 0.83em;">{{ page.description }}</h6>
  {% if page.address %}
      <h6 class="m-0 mb-2" style="font-size: 0.83em;">{{ page.address }}</h6>
  {% endif %}
</div>

<!-- Introduction -->

<div style="display: flex; flex-wrap: wrap;">
    <div class="text-justify p-0">
        <div class="col-xs-12 col-sm-6 p-0 pt-2 pb-sm-2 pb-4 pl-sm-4 text-center" style="float: right;">
          <img class="profile-img img-responsive" src="{{ 'prof_pic.jpg' | prepend: '/assets/img/' | prepend: site.baseurl | prepend: site.url }}">
        </div>

        <p>
            I am a PhD student in the <a href="http://www.ml.cmu.edu/" target="_blank">Machine Learning Department</a> at <a href="http://www.cmu.edu/" target="_blank">Carnegie Mellon University</a>, co-advised by <a href="http://www.cs.cmu.edu/~tom/" target="_blank">Tom Mitchell</a> and <a href="http://www.cs.cmu.edu/~bapoczos/" target="_blank">Barnabàs Pòczos</a>.
        </p>
        
        <p>
            My PhD research focuses on developing algorithms for machine learning, mainly focused on semi-supervised learning, curriculum learning, multitask learning, and graph-based problems.
            I am also passionate about applying machine learning methods in neuroscience, in order to study how the brain understands language and controls speech.
            Previously, I did some research in Computer Vision, with the goal of detecting and tracking objects in videos.
        </p>
    </div>
</div>

<div class="col text-justify p-0">
    <p>
        Before I joined CMU, I graduated with an <a href="https://www.cst.cam.ac.uk/admissions/acs" target="_blank">M.Phil. in Advanced Computer Science</a>
        from the <a href="https://www.cam.ac.uk/" target="_blank">University of Cambridge</a>, UK.
        In my Master's thesis I used Machine Learning methods to detect and align chromosomes in microscope images,
        advised by <a href="https://www.cl.cam.ac.uk/~pl219/" target="_blank">Pietro Lió</a>.
    </p>
</div>

<!-- News -->
<div class="news mt-3 p-0">
  <h1 class="title mb-4 p-0">news</h1>
  {% assign news = site.news | reverse %}
  {% for item in news limit: site.news_limit %}
    <div class="row p-0">
      <div class="col-sm-2 p-0">
        <span class="badge light-green darken-1 font-weight-bold text-uppercase align-middle date ml-3">
          {{ item.date | date: "%b %-d, %Y" }}
        </span>
      </div>
      <div class="col-sm-10 mt-2 mt-sm-0 ml-3 ml-md-0 p-0 font-weight-light text">
        <p>{{ item.content | remove: '<p>' | remove: '</p>' | emojify }}</p>
      </div>
    </div>
  {% endfor %}
</div>

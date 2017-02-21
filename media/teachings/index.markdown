---
title: Teachings
layout: media-page
header-image: assets/img/beliefs-bg.jpg
image: "/assets/img/beliefs-bg.jpg"
---

<div class="row justify-content-center">
    <div class="col-md-10 text-center">
        <h1>{{ page.title }}</h1>  
    </div>
</div>
<div class="row justify-content-center">
  {% assign items = site.teachings | sort: 'date' | reverse %}
  {% for item in items %}
  <div class="col-md-4">
    <div class="card">
      <div class="thumb-crop">
        <a href="{{ item.url | prepend: site.baseurl }}"><img class="card-img-top" src="{{ item.image }}" alt="{{ item.title }}" /></a>
      </div>
      <div class="card-block">
        <h4 class="card-text"><a href="{{ item.url | absolute_url }}">{{ item.title }}</a></h4>
        <span class="post-meta">{{ item.date | date: "%b %-d, %Y" }}</span>
      </div>
    </div>
  </div>
  {% endfor %}
</div>
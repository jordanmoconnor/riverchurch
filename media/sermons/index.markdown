---
title: Sermons
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
{% for item in site.sermons reversed %}
<div class="col-md-4">
    <div class="card">
      {% if item.video_id[0] != "none" %}
      <div class="thumb-crop">
        <a href="{{ item.url | prepend: site.baseurl }}"><img class="card-img-top" src="https://img.youtube.com/vi/{{ item.video_id[0] }}/maxresdefault.jpg" alt="{{ item.title }}" /></a>
      </div>
      {% else %}
      <div class="thumb-crop">
        <a href="{{ item.url | prepend: site.baseurl }}"><img class="card-img-top" src="{{ item.image }}" alt="{{ item.title }}" /></a>
      </div>
      {% endif %}
      <div class="card-block">
        <h4 class="card-text"><a href="{{ item.url | absolute_url }}">{{ item.title }}</a></h4>
        <span class="post-meta">{{ item.date | date: "%b %-d, %Y" }}</span>
      </div>
    </div>
</div>
{% endfor %}
</div>
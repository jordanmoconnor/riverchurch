---
title: Sermons
layout: media-page
header-image: assets/img/beliefs-bg.jpg
image: "/assets/img/beliefs-bg.jpg"
navigation_weight: 4
---

<div class="row justify-content-center">
    <div class="col-md-10 text-center">
        <h1>{{ page.title }}</h1>  
    </div>
</div>
<div class="row justify-content-center">
  <div class="col-md-10 text-center">
    <p>You can find our sermons on your favorite podcast app by searching "River Rochester".</p>
    <a class="btn btn-xl-dark" href="https://geo.itunes.apple.com/us/podcast/river-rochester/id1182211082?mt=2">iTunes</a>
    <a class="btn btn-xl-dark" href="http://www.stitcher.com/podcast/river-rochester"> Stitcher</a>
    <a class="btn btn-xl-dark" href="http://pca.st/dIb4"> Pocket Casts</a>
    <a class="btn btn-xl-dark" href="https://overcast.fm/itunes1182211082/river-rochester"> Overcast</a>
    <a class="btn btn-xl-dark" href="https://goo.gl/app/playmusic?ibi=com.google.PlayMusic&isi=691797987&ius=googleplaymusic&link=https://play.google.com/music/m/Ijbddmopd735kwqpa5reingncou?t%3DRiver_Rochester"> Google Play</a>
  </div>
</div>
<div class="row justify-content-center">
{% for item in site.sermons reversed %}
<div class="col-md-4">
    <div class="card">
      {% if item.video_id[0] != "none" %}
      <div class="thumb-crop">
        <a href="{{ item.url | absolute_url }}"><img class="card-img-top" src="https://img.youtube.com/vi/{{ item.video_id[0] }}/maxresdefault.jpg" alt="{{ item.title }}" /></a>
      </div>
      {% else %}
      <div class="thumb-crop">
        <a href="{{ item.url | absolute_url }}"><img class="card-img-top" src="{{ item.image | absolute_url }}" alt="{{ item.title }}" /></a>
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

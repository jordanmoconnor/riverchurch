---
title: Media
layout: media-page
navigation_weight: 2
---

<div class="row justify-content-center">
  <div class="col-md-6 text-center">
    <h1 class="">Latest Sermons</h1>
    <a href="{{ '/media/sermons' | prepend: site.baseurl }}"><button class="btn btn-xl-dark">View All Sermons</button></a>
  </div>
</div>
<div class="row justify-content-center">
  {% assign items = site.sermons | sort: 'date' | reverse %}
  {% for item in items  limit:6 %}
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
<div class="row justify-content-center">
  <div class="col-md-10 text-center">
    <hr>
  </div>
</div>
<div class="row justify-content-center">
  <div class="col-md-8 text-center">
    <h2>Sermon Podcast</h2>
    <p>You can find our sermons on your favorite podcast app by searching "River Rochester".</p>
    <a class="btn btn-xl-dark" href="https://geo.itunes.apple.com/us/podcast/river-rochester/id1182211082?mt=2">iTunes</a>
    <a class="btn btn-xl-dark" href="http://www.stitcher.com/podcast/river-rochester"> Stitcher</a>
    <a class="btn btn-xl-dark" href="http://pca.st/dIb4"> Pocket Casts</a>
    <a class="btn btn-xl-dark" href="https://overcast.fm/itunes1182211082/river-rochester"> Overcast</a>
    <a class="btn btn-xl-dark" href="https://goo.gl/app/playmusic?ibi=com.google.PlayMusic&isi=691797987&ius=googleplaymusic&link=https://play.google.com/music/m/Ijbddmopd735kwqpa5reingncou?t%3DRiver_Rochester"> Google Play</a>
  </div>
</div>
<div class="row justify-content-center">
  <div class="col-md-10 text-center">
    <hr>
  </div>
</div>
<div class="row justify-content-center">
  <div class="col-md-6 text-center">
    <h2>Latest <a href="{{ 'media/teachings/' | absolute_url }}">Teachings</a></h2>
  </div>
</div>
<div class="row justify-content-center">
  {% assign items = site.teachings | sort: 'date' | reverse %}
  {% for item in items  limit: 3 %}
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
<div class="row justify-content-center">
  <div class="col-md-10 text-center">
    <hr>
  </div>
</div>
<div class="row justify-content-center">
  <div class="col-md-6 text-center">
    <h2>Latest <a href="{{ 'media/blog/' | absolute_url }}">Posts</a></h2>
  </div>
</div>
<div class="row justify-content-center">
  {% for item in site.posts  limit: 3 %}
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

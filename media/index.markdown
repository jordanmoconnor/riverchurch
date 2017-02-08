---
title: Media
layout: post
---

<div class="home text-center">
    <div class="container">
      <h1>Latest Sermons</h1>
      <a href="{{ 'media/sermons/' | absolute_url }}"><button class="btn btn-primary btn-xl-dark" type="button" name="button">View All Sermons</button></a>
      <div class="col-sm-10 col-sm-offset-1">
      <hr>
      <h2>Sermon Podcast</h2>
        <p>You can find our sermons on your favorite podcast app by searching "River Rochester".</p>
        <ul class="list-inline text-center">
            <li><a href="https://geo.itunes.apple.com/us/podcast/river-rochester/id1182211082?mt=2">iTunes</a></li> |
            <li><a href="http://www.stitcher.com/podcast/river-rochester"> Stitcher</a></li> |
            <li><a href="http://pca.st/dIb4"> Pocket Casts</a></li> |
            <li><a href="https://overcast.fm/itunes1182211082/river-rochester"> Overcast</a></li> |
            <li><a href="https://goo.gl/app/playmusic?ibi=com.google.PlayMusic&isi=691797987&ius=googleplaymusic&link=https://play.google.com/music/m/Ijbddmopd735kwqpa5reingncou?t%3DRiver_Rochester"> Google Play</a></li>
        </ul>
        <hr>
      </div>
      <div class="home text-center">
          <ul class="post-list">
            {% assign items = site.sermons | sort: 'date' | reverse %}
            {% for item in items  limit:6 %}
              <li>
                  <div class="col-sm-6 col-sm-offset-3">
                    <h3><a href="{{ item.url | prepend: site.baseurl }}">{{ item.title }}</a></h3>
                    <span class="post-meta">{{ item.date | date: "%b %-d, %Y" }}</span>
                      {% if item.video_id[0] != "none" %}
                      <div class="thumb-crop">
                        <a href="{{ item.url | prepend: site.baseurl }}"><img src="https://img.youtube.com/vi/{{ item.video_id[0] }}/maxresdefault.jpg" alt="" /></a>
                      </div>
                      {% else %}
                      <div class="thumb-crop">
                        <a href="{{ item.url | prepend: site.baseurl }}"><img src="../assets/img/logos/black-background.png" alt="" /></a>
                      </div>
                      {% endif %}
                  </div>
              </li>
            {% endfor %}
          </ul>
        </div>
    </div>
    <div class="container">
    <hr>
    <h1>Latest Teachings</h1>
      <a href="{{ 'media/teachings/' | absolute_url }}"><button class="btn btn-primary btn-xl-dark" type="button" name="button">View All Teachings</button></a>
      <div class="home text-center">
          <ul class="post-list">
            {% assign items = site.teachings | sort: 'date' | reverse %}
            {% for item in items  limit:5 %}
              <li>
                <div class="container-fluid">
                  <div class="col-md-12">
                    <h2><a href="{{ item.url | prepend: site.baseurl }}">{{ item.title }}</a></h2>
                      <span class="post-meta">{{ item.date | date: "%b %-d, %Y" }}</span>
                  </div>
                </div>
              </li>
            {% endfor %}
          </ul>
        </div>
        <hr>
    </div>
    <div class="container">
    <h1>Latest Blog Posts</h1>
      <a href="{{ 'media/blog/' | absolute_url }}"><button class="btn btn-primary btn-xl-dark" type="button" name="button">View All Blog Posts</button></a>
      <div class="home text-center">
          <ul class="post-list">
            {% for post in site.posts limit:5 %}
              <li>
                <div class="container-fluid">
                  <div class="col-md-12">
                    <h2><a href="{{ post.url | prepend: site.baseurl }}">{{ post.title }}</a></h2>
                      <span class="post-meta">{{ post.date | date: "%b %-d, %Y" }}</span>
                  </div>
                </div>
              </li>
            {% endfor %}
          </ul>
        </div>
        <hr>
    </div>
</div>

---
title: Sermons
layout: media-page
header-image: assets/img/beliefs-bg.jpg
image: "/assets/img/beliefs-bg.jpg"
---

<h1>{{ page.title }}</h1>  
{% for post in site.sermons reversed %}
{% capture currentyear %}{{post.date | date: "%Y"}}{% endcapture %}
{% if currentyear != year %}
{% unless forloop.first %}</ul>{% endunless %}
<h5>{{ currentyear }}</h5>
<ul class="posts">
{% capture year %}{{currentyear}}{% endcapture %}
{% endif %}
<li><a href="{{ post.url | prepend: site.baseurl }}"><h3>{{ post.title }}</h3></a><span class="post-meta">{{ post.date | date: "%b %-d, %Y" }}</span></li>
{% endfor %}
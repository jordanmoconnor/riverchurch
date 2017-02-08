---
title: Teachings
layout: media-page
header-image: assets/img/beliefs-bg.jpg
image: "/assets/img/beliefs-bg.jpg"
---

<h1>{{ page.title }}</h1>  
{% for teaching in site.teachings reversed %}
{% capture currentyear %}{{teaching.date | date: "%Y"}}{% endcapture %}
{% if currentyear != year %}
{% unless forloop.first %}</ul>{% endunless %}
<h5>{{ currentyear }}</h5>
<ul class="posts">
{% capture year %}{{currentyear}}{% endcapture %}
{% endif %}
<li><a href="{{ teaching.url | prepend: site.baseurl }}"><h3>{{ teaching.title }}</h3></a><span class="post-meta">{{ teaching.date | date: "%b %-d, %Y" }}</span></li>
{% endfor %}
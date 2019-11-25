---
layout: base
title: Archive
permalink: /archive/
---

<section id="wrapper">
  <header id="header">
  <a href="{{ site.url }}" id="title">
  <img src="{{ site.url }}/assets/img/logo.png" style="width: 3em">
  </a>
  </header> <!--header-->

	<ul id="archive-list">
		{% for post in site.posts %}

			{% capture month %}{{ post.date | date: '%m%Y' }}{% endcapture %}
    		{% capture nmonth %}{{ post.next.date | date: '%m%Y' }}{% endcapture %}
        		{% if month != nmonth %}
            		<h2 class="month">{{ post.date | date: '%B %Y' }}</h2>
        		{% endif %}

		<li> 
        	<a href='{{ post.url | prepend: site.url }}'><aside class="dates">{{ post.date | date: "%b %d" }}</aside></a>
        	<a href='{{ post.url | prepend: site.url }}'>{{ post.title }}</a>
		</li>
		{% endfor %}
	</ul> <!--post-list-->

  <footer id="footer">
   <p class="small">Lorem ipsum dolor, sit <a href="http://www.twitter.com/">@loremipsum</a>.</p>
  </footer>
</section> <!--wrapper-->

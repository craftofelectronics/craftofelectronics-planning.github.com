---
layout: homepage
title: Make. Measure. Learn.
---
<div class="row">
	
<div class="span6">

<h2>Blog</h2>
<!-- Blog Posts go here -->
	{% for post in site.posts %}	
		  <h3><a href="{{ post.url }}">{{ post.title }}</a></h3>
          <i>{{ post.summary }}</i>
		  <p><small>{{ post.date | date: "%B %e, %Y" }} posted in <b>{{ post.category }}</b> </small></p>
	{% endfor %}			

</div>

<div class="span5 offset1">

<h2>Tweets</h2>
<!-- Set site.twitter to false if not desired -->
{% if site.twitter %}
<h2><a href="https://twitter.com/#!/{{ site.twitter }}">@{{ site.twitter }}</a></h2>
<div class="tweet"></div>
{% endif %}

</div> <!-- span5 -->
</div> <!-- row -->

<div class="row">
<div class="well">
<h2>Can I help?</h2>
<p>Yeah! We're in the early stages, so it's a glorious mess; hop right in on the <a href="http://groups.google.com/group/craftofelectronics">mailing list</a> and introduce yourself, and we'll get you started.
</p>
</div>
</div>
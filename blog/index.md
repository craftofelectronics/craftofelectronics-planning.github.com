---
layout : page
title : Project Blog
---

<div class="row">
	<div class="span2">&nbsp;</div>
	<div class="span8">
	{% for post in site.posts %}	
		<h3><b>[ {{ post.date | date: "%Y %m %d" }} ]</b> <a href="{{ post.url }}">{{ post.title }}</a></h3>
		<p><i>{{ post.summary }}</i></p>
		<p><small>Posted in <b>{{ post.category }}</b> by <b> {{ post.author }} </b> </small></p>
	{% endfor %}			
	</div>
	<div class="span2">&nbsp;</div>
</div>

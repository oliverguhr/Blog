---
layout: page
title: Home
---
{% include JB/setup %}

{% assign englishPosts = site.posts | where: "language", "en" %}
{% for post in englishPosts limit:20 %}
<article class="box">				
				<div class="content">
					<h2><a href="{{ BASE_PATH }}{{ post.url }}">{{ post.title }}</a></h2>
					<p class="text">{{ post.description }}</p>
					<p class="text-small"><i>Posted on {{ post.date | date_to_string }} by {{ post.author }}</i></p>
					<a class="button" href="{{ BASE_PATH }}{{ post.url }}">Read Full Post</a>
				</div>
</article>
{% endfor %}
<!--
<div>
  {% assign englishPosts = site.posts | where: "language", "en" %}
  {% for post in englishPosts limit:20 %}
	<div class="row">
		<div class="col-md-12">
			<a href="{{ BASE_PATH }}{{ post.url }}"><h2>{{ post.title }}</h2></a>
			<p>{{ post.description }}</p>
			<p><i>Posted on {{ post.date | date_to_string }} by {{ post.author }}</i></p>
			<hr>
		</div>
	</div>
  {% endfor %}
</div>-->

---
layout: default
---


{% for post in site.posts limit:5 %}
  <article class="{% if forloop.first %}first{% elsif forloop.last %}last{% else %}middle{% endif %}">
		<div class="article-head">
			<h2 class="title"><a href="{{ site.url }}{{ post.url }}" class="js-pjax">{{ post.title }}</a></h2>
			<p class="date">{{ post.date | date: "%b %d, %Y" }}</p>
		</div><!--/.article-head-->
		<div class="article-content">
		{{ post.content }}		

		{% unless forloop.last %}    
        	<hr>
    	{% endunless %}

		</div><!--/.article-content-->
	</article>
	

{% endfor %}
---
layout: page
title: in the open
tagline: from the newsroom
description: My name is Annabel Church and I am a Knight-Mozilla OpenNews Fellow. I am coder embeded in the newsroom at Zeit Online.
---

{% include JB/setup %}

<section class="posts">
	<ol>
		{% for post in site.posts limit:2 %}
		<li>
			<article>
				<header>	
					{% if post.topic %}<span class="topic">{{ post.topic }}</span>{% endif %}
					<a href="{{ BASE_PATH }}{{ post.url }}">
			    		<h3> {{ post.title }} </h3>
			    	<!-- <img src="/images/postimages/trailpics-large/wii-u.jpg" alt=""> --></a>
			    	<!-- {% unless post.tags == empty %}
					    <ul class="tags inline">
					      {% assign tags_list = post.tags %}
					      {% include JB/tags_list %}
					    </ul>
					{% endunless %}  -->
			    </header>
			    {% if post.teaser %}
				    <p class="summary">
				    	<span class="date">{{ post.date | date: "%d %B %Y" }} · </span>
						<a href="{{ BASE_PATH }}{{ post.url }}">{{ post.teaser }}</a>
				    </p>
			    {% endif %}
			</article>
		</li>
		{% endfor %}
	</ol>
</section>



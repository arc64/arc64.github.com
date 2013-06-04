---
layout: page
title: in the open
tagline: from the newsroom
description: My name is Annabel Church and I am a Knight-Mozilla OpenNews Fellow. I am coder embeded in the newsroom at Zeit Online.
---

{% include JB/setup %}

<section class="posts">
	<ol>
		{% for post in site.posts limit:5 %}
		<li>
			<article>
				<header>	
					{% if post.category %}<span class="category">{{ post.category }}</span>{% endif %}
					<a title="read more on {{ post.title }}" href="{{ BASE_PATH }}{{ post.url }}">
			    		<h3> {{ post.title }} </h3>
			   		</a>
			    	<!-- {% unless post.tags == empty %}
					    <ul class="tags inline">
					      {% assign tags_list = post.tags %}
					      {% include JB/tags_list %}
					    </ul>
					{% endunless %}  -->
			    </header>
			    {% if post.teaser %}
				    <p class="teaser">
				    	<span class="date">{{ post.date | date: "%d %B %Y" }} </span> &sdot;
						<a title="read more on {{ post.title }}" href="{{ BASE_PATH }}{{ post.url }}"> {{ post.teaser }} <span class="more">&rsaquo;&rsaquo;</span></a>
				    </p>
			    {% endif %}
			</article>
		</li>
		{% endfor %}
	</ol>
</section>


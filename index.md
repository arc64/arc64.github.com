---
layout: page
title: in the open
tagline: from the newsroom
description: My name is Annabel Church and I am a Knight-Mozilla OpenNews Fellow. I am coder embeded in the newsroom at Zeit Online.
---

{% include JB/setup %}

<section class="posts">

		{% for post in site.posts limit:1 %}

			<article>
				<header>

					<!-- <a title="read more on {{ post.title }}" href="{{ BASE_PATH }}{{ post.url }}">
			    		<h3> {{ post.title }} </h3>
			   		</a> -->

			    </header>
					{{ post.content }}
			    	{% unless post.tags == empty %}
					    <ul class="tags inline">
					      {% assign tags_list = post.tags %}
					      {% include JB/tags_list %}
					    </ul>
					{% endunless %}
					{% if post.category %}<span class="category">{{ post.category }}</span>{% endif %}
			</article>

		{% endfor %}

</section>


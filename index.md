---
layout: page
title: me
tagline: coder, coffee drinker
description:
---

{% include JB/setup %}

<section class="posts">

		{% for post in site.posts limit:1 %}

			<article>
				<header>

					<!-- <a title="read more on {{ post.title }}" href="{{ BASE_PATH }}{{ post.url }}"> -->
			    		<h1> {{ post.title | markdownify | remove: '<p>' | remove: '</p>'}} {% if post.tagline %}<small>{{ post.tagline }}</small>{% endif %}</h1>
			   		<!-- </a> -->

			    </header>
                    <div class="column">
					{{ post.content }}
                    </div>
			    	<!-- {% unless post.tags == empty %}
					    <ul class="tags inline">
					      {% assign tags_list = post.tags %}
					      {% include JB/tags_list %}
					    </ul>
					{% endunless %}
					{% if post.category %}<span class="category">{{ post.category }}</span>{% endif %} -->
			</article>

		{% endfor %}

</section>

<section>
    <nav class="column">
        <a href="/events" class="pull">
			Events where I've been a <strong>speaker</strong>
        </a>
        <a href="/projects" class="pull">
		 	<strong>Projects</strong> I have worked on
        </a>
        <a href="/about" class="pull">
			A few more things <strong>about</strong> me
        </a>
    </nav>
</section>

<section>
<figure class="quote">

<blockquote cite="Grace Hopper">Humans are allergic to change. They love to say, 'We've always done it this way.' I try to fight that. That's why I have a clock on my wall that runs counter-clockwise. &mdash;<strong>Grace Hopper</strong></blockquote>

</figure>

</section>

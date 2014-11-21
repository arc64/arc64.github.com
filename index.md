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

<blockquote cite="Dr. Seuss">You have brains in your head. You have feet in your shoes. You can steer yourself in any direction you choose. You're on your own, and you know what you know. And you are the guy who'll decide where to go. &mdash;<strong>Dr. Seuss</strong></blockquote>

</figure>

</section>

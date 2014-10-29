---
layout: page
title: in the open
tagline: from the newsroom
description:
---

{% include JB/setup %}

<section class="posts">

		{% for post in site.posts limit:1 %}

			<article>
				<header>

					<a title="read more on {{ post.title }}" href="{{ BASE_PATH }}{{ post.url }}">
			    		<h1> {{ post.title | markdownify | remove: '<p>' | remove: '</p>'}} </h1>
			   		</a>

			    </header>
					{{ post.content }}
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
	   <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean quam massa, pulvinar a nunc eget, bibendum
varius metus ultrices nec. Nullam dapibus libero eu lobortis egestas. Nulla at tortor aliquam, varius purus vitae, bibendum tellus. Pellentesque efficitur ligula in lorem pharetra fringilla. Nulla varius felis ornare pharetra lacinia.</p>
</section>

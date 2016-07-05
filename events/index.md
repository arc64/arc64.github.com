---
layout: page
title: Attended with **enthusiasm**
tagline: remembered fondly
description:
---

{% include themes/intheopen/includes/title.html %}

<section class="column" markdown="1">


{% assign events = site.data.events | group_by: "year" %}
{% for group in events %}
<h3>{{group.name}}</h3>
<ul class="events">
    {% assign eventsSorted = group.items  | sort: "month" | reverse %}
    {% assign eventsGrouped = eventsSorted | group_by:"month-name" %}

    {% for item in eventsSorted %}

<!-- | group_by:"month"  -->
    <li>{% if item.url %}<a href="{{item.url}}" title="{{item.event}}">{% endif %} {{item.event}} {% if item.url %}</a>{% endif %} &mdash; {{item.month-name}} {% if item.role %}<i class="fa fa-child" aria-hidden="true"></i><span class="fallback-text">{{item.role}}</span>{% endif %}</li>
    {% endfor %}
</ul>
{% endfor %}

[<i class="fa fa-child"></i>] Speaker / Hacker / Mentor / Hiker

<h3>My favourites</h3>

{% assign events = site.data.events | group_by: "favourite" %}
{% for group in events %}
{% if group.name == 'true' %}
<ul class="events">
    {% for item in group.items %}
    <li>{% if item.url %}<a href="{{item.url}}" title="{{item.event}}">{% endif %} {{item.event}} {% if item.url %}</a>{% endif %} {% if item.favourite %}<i class="fa fa-heart" aria-hidden="true"></i><span class="fallback-text">favourite</span>{% endif %}</li>
    {% endfor %}
</ul>
{% endif %}
{% endfor %}

[<i class="fa fa-heart"></i>]  Wonderful people / Great speakers/ Lovely place / Exciting / Safe

</section>


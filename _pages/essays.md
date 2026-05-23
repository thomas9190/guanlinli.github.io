---
layout: archive
permalink: /essays/
title: "Essays"
author_profile: true
redirect_from:
  - /opinion/
---

{% include base_path %}

{% if site.categories.essays %}
{% capture written_year %}'None'{% endcapture %}
{% for post in site.categories.essays %}
{% capture year %}{{ post.date | date: '%Y' }}{% endcapture %}
{% if year != written_year %}
<h2 id="{{ year | slugify }}" class="archive__subtitle">{{ year }}</h2>
{% capture written_year %}{{ year }}{% endcapture %}
{% endif %}
{% include archive-single.html %}
{% if post.essay_image %}
<figure class="essay-archive-image">
  <a href="{{ base_path }}{{ post.url }}">
    <img src="{{ post.essay_image | prepend: base_path }}" alt="{{ post.essay_image_alt | default: post.title }}">
  </a>
</figure>
{% endif %}
{% endfor %}
{% else %}
<p>No essays yet.</p>
{% endif %}

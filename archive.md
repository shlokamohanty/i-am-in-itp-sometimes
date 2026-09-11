---
layout: default
title: archive
permalink: /archive.html
---

<p class="archive-intro">everything, in order.</p>

{% assign postsByYear = site.posts | group_by_exp: "post", "post.date | date: '%Y'" %}

{% for year in postsByYear %}
<div class="archive-year">
  <div class="section-head">
    <span class="section-label">{{ year.name }}</span>
    <div class="section-rule"></div>
  </div>
  <ul class="post-list">
    {% for post in year.items %}
    <li>
      <a href="{{ post.url | relative_url }}" class="post-row">
        <span class="post-row-date">{{ post.date | date: "%b %d, %Y" }}</span>
        <div class="post-row-body">
          <div class="post-row-title">{{ post.title }}</div>
        </div>
        {% for tag in post.tags %}
          {% unless tag == "Other" %}
            <span class="post-tag">{{ tag | downcase }}</span>
          {% endunless %}
        {% endfor %}
      </a>
    </li>
    {% endfor %}
  </ul>
</div>
{% endfor %}

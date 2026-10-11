---
layout: page
title: tonGues articles
---

Write-ups about building **tonGues** — a language-exchange messenger with chat,
voice and video calls, media messages, and on-the-fly translation and
transcription. Flutter on the client, FastAPI + PostgreSQL on the server.

## Posts

{% assign posts = site.pages | where_exp: "p", "p.path contains 'articles/'" | sort: "path" | reverse %}
<ul class="post-list">
{% for post in posts %}
  <li>
    <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
    {% if post.description %}<p>{{ post.description }}</p>{% endif %}
  </li>
{% endfor %}
</ul>

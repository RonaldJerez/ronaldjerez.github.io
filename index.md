---
layout: page
title: Thoughts
order: 1
class: w3-sand
---

{% for post in site.posts %}
## {{ post.title | escape }}
{{ post.excerpt }}
[Read More...]({{ post.url | relative_url }})
{% endfor %}
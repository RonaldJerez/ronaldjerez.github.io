---
layout: page
title: Thoughts
order: 1
class: w3-white
---

{% for post in site.posts %}
<article itemprop="blogPost" itemscope itemtype="http://schema.org/BlogPosting">
    {% include postHeader.html %}
    {{ post.excerpt }}
    <a class="w3-btn w3-red post-link {% if forloop.last %}w3-margin-bottom{% endif %}" href="{{ post.url | relative_url }}" itemprop="mainEntityOfPage url">Read More...</a>
    {% unless forloop.last %}
    <hr class="post-seperator">
    {% endunless %}
</article>
{% endfor %}
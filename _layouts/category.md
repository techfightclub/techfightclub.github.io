---
layout: slim
---

<h2> 
    <span class="category {{ page.title | remove: " " | downcase }}">{{ page.title }}</span>
</h2>

{% for page in site.categories[page.title] %}
    {% include item.md %}
{% endfor %}
---
layout: default
---

<section>
    <h2>Categories</h2>
    <p>{{ site.content | markdownify }}</p>
    <p>
    {% for category in site.categories %}
        <a href="/categories/{{ category[0] | slugify }}.html">
            <span class="category {{ category[0] | remove: " " | downcase }}">{{ category[0] }}</span>
        </a>
    {% endfor %}
    </p>
    <p>{{ site.contribute | markdownify }}</p>
</section>

<section>
    <h2>Lastest</h2>
    {% for page in site.posts limit: 5 %}
        {% include item.md %}
    {% endfor %}
</section>
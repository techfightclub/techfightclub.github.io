<section>
    <h2><a href="{{ page.link }}" target="_blank" title="{{ page.title }}">{{ page.title }}</a></h2>
    <p>
        {% for category in page.categories %}
        <a href="/categories/{{ category | slugify }}.html">
            <span class="category {{ category | remove: " " | downcase }}">{{ category }}</span>
        </a>
        {% endfor %}
    </p>
        {{ page.content }}
    <p>Link: <a href="{{ page.link }}" target="_blank" title="{{ page.title }}">{{ page.title }}</a></p>
 </section>
<h1>Categories</h1>
<p>{{ site.content | markdownify }}<p>

{% assign all_tags = site.data.content | map: "tags" | uniq | sort_natural %}
{% for tag in all_tags %}
  <h2>{{ tag | capitalize }}</h2>
  <ul class="content">
  {% for item in site.data.content %}
    {% for item_tag in item.tags %}
      {% if item_tag == tag %}
        <li>
          <a href="{{ item.href }}" target="_blank">{{ item.title }}</a>
          {% for tag_to_render in item.tags %}
            <span class="{{ tag_to_render | remove: " " | downcase }}">{{ tag_to_render }}</span>
          {% endfor %}
        </li>
      {% endif %}
    {% endfor %}
  {% endfor %}
  </ul>
{% endfor %}
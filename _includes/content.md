<h1>Categories</h1>
<p>{{ site.content | markdownify }}<p>

{% assign all_tags = site.data.content | map: "tags" | uniq | sort_natural %}
{% for tag in all_tags %}
  <h2>{{ tag }}</h2>
  <ul class="content">
  {% for item in site.data.content %}
    {% for item_tag in item.tags %}
      {% if item_tag == tag %}
        <li>
          <span title="{{ item.type | capitalize }}" class="gg-{{ item.type | downcase }} "></span>
          <a href="{{ item.href }}" target="_blank">{{ item.title }}</a>
          <small>
          {% for tag_to_render in item.tags %}
            <span class="tag {{ tag_to_render | remove: " " | downcase }}">{{ tag_to_render }}</span>
          {% endfor %}
          </small>
        </li>
      {% endif %}
    {% endfor %}
  {% endfor %}
  </ul>
{% endfor %}
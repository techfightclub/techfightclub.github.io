---
layout: custom_default22
---

{% case site.color-scheme %}
  {% when "", nil, false, 0, empty %}
    {% assign ColorScheme = "auto" %}
  {% else %}
    {% assign ColorScheme = site.color-scheme %}
{% endcase %}

<!DOCTYPE html>
<html lang="{{ site.lang | default: "en-US" }}">
  <head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1">

{% seo %}
    <link rel="stylesheet" href="{{ "/assets/css/colors-ColorScheme.css?v=" | append: site.github.build_revision | relative_url | replace: "ColorScheme", ColorScheme }}">
    <link rel="stylesheet" href="{{ "/assets/css/style.css?v="              | append: site.github.build_revision | relative_url }}">
    <link rel="stylesheet" href="{{ "/assets/css/custom.css?v="              | append: site.github.build_revision | relative_url }}">
    <link rel="stylesheet" href="{{ "/assets/css/icons.css?v="              | append: site.github.build_revision | relative_url }}">
  </head>
  <body>
    <div class="wrapper">
      <header>
      </header>
      <section>
        {{ content }}
      </section>
      <section>
        {% include content.md %}
      </section>
      <footer>
        <p><small>Hosted on GitHub Pages &mdash; Credits to <a href="https://github.com/godalming123">godalming123 (Basic theme)</a></small></p>
      </footer>
    </div>
  </body>
</html>
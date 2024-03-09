{% include header.md %}
<section>
    {{ site.headline | markdownify }}
    {{ site.story | markdownify }}
</section>
{{ content }}
{% include footer.md %}
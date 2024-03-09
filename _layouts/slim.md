{% include header.md %}
<section>
    {{ site.headline | markdownify }}
    <p>{{ site.contribute | markdownify }}</p>
    <a href="/">&larr; Back (to overview)</a>
</section>
{{ content }}
{% include footer.md %}
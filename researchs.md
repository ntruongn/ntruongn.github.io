---
title: home
layout: page
command: ls
---

<div class="post-list">
    <ul>
    {% for p in site.researchs %}
        {% if p.title != nil and p.title != "home" %}
            {% if p.layout == "post" %}
                <li><a href="{{ p.url | relative_url }}">
                    ./ [{{ p.date | default: site.time | date: date_format }}] - {{ p.title }}
                </a></li>
            {% endif %}
        {% endif %}
    {% endfor %}
    </ul>
</div>
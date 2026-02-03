---
title: "Publications"
permalink: /publications-cv/
author_profile: true
---

{% assign my_name = "Shuai Shao" %}
{% assign pubs = site.publications | sort: "date" | reverse %}

<ol>
{% for p in pubs %}
  <li>
    <strong>{{ p.title }}</strong>.<br/>
    {{ p.authors | replace: my_name, "<strong>" | append: my_name | append: "</strong>" }}.
    {% if p.venue %}<em>{{ p.venue }}</em>,{% endif %}
    {{ p.year }}.
  </li>
{% endfor %}
</ol>
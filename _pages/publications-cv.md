---
title: "Publications"
permalink: /publications-cv/
author_profile: true
---

{% assign pubs = site.publications | sort: "date" | reverse %}

<ol>
{% for p in pubs %}
  <li>
    <strong>{{ p.title }}</strong>.
    {{ p.authors }}.
    {% if p.venue %}<em>{{ p.venue }}</em>,{% endif %}
    {{ p.year }}.
  </li>
{% endfor %}
</ol>
---
permalink: /
title: "Shuai Shao"
author_profile: true
redirect_from:
  - /about/
  - /about.html
---

I am a PhD student in Computer Science at the University of Connecticut (UConn).

My research focuses on **concurrent bug localization**, **static analysis**, and **large language model–based software engineering**.  
I am particularly interested in developing practical and explainable techniques that bridge **bug reports** and **source code** for understanding and locating concurrency bugs in large-scale systems.

---

## Recent Publications

{% assign my_name = "Shuai Shao" %}
{% assign pubs = site.publications | sort: "date" | reverse %}

<ol>

{%- comment -%} Published / Accepted {%- endcomment -%}
{% assign count = 0 %}
{% for p in pubs %}
  {% if p.venue contains "arXiv" %}
    {% continue %}
  {% endif %}
  {% if count >= 10 %}
    {% break %}
  {% endif %}
  <li>
    <strong>{{ p.title }}</strong>.<br/>
    {{ p.authors | replace: my_name, "<strong>" | append: my_name | append: "</strong>" }}.<br/>
    <em>{{ p.venue }}</em>, {{ p.year }}.
  </li>
  {% assign count = count | plus: 1 %}
{% endfor %}

{%- comment -%} Fill with arXiv if < 10 {%- endcomment -%}
{% for p in pubs %}
  {% if count >= 10 %}
    {% break %}
  {% endif %}
  {% unless p.venue contains "arXiv" %}
    {% continue %}
  {% endunless %}
  <li>
    <strong>{{ p.title }}</strong>.<br/>
    {{ p.authors | replace: my_name, "<strong>" | append: my_name | append: "</strong>" }}.<br/>
    <em>{{ p.venue }}</em>, {{ p.year }}.
  </li>
  {% assign count = count | plus: 1 %}
{% endfor %}

</ol>

<p>
  <a href="/publications-cv/">Full publication list</a>
</p>

--

## Work Experience

- **Spring 2026**: Teaching Assistant  
  *CSE 3400 / CSE 5850 — Introduction to Cryptography and Cybersecurity*

- **Fall 2025**: Teaching Assistant  
  *CSE 3400 / CSE 5850 — Introduction to Cryptography and Cybersecurity*
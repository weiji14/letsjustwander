---
title: Let's Just Wander
subtitle: A blog to jot down wanderlusting thoughts with a heck of a mindset.
layout: base.njk
---

## Posts

<ul>
{%- for post in collections.post reversed sort_by:date -%}
  <li>
    <a href={{ post.url }}>{{ post.data.title }}</a>
    <time> ~ <small>{{ post.data.date | date: "%d/%m/%Y" }}</small></time>
  </li>
{%- endfor -%}
</ul>

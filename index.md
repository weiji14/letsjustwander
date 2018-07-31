---
title: Let's Just Wander
subtitle: A blog to jot down wanderlusting thoughts with a heck of a mindset.
layout: base.njk
---

## Posts

<ul>
{%- for post in collections.post -%}
  <li>
    <a href={{ post.url }}>{{ post.data.title }}</a>
  </li>
{%- endfor -%}
</ul>

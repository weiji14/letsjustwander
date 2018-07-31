# Let's Just Wander

Welcome to this blog!

## Posts

<ul>
{%- for post in collections.post -%}
  <li>
    <a href={{ post.url }}>{{ post.data.title }}</a>
  </li>
{%- endfor -%}
</ul>

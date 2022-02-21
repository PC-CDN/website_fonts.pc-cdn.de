---
layout: default 
permalink: /myfontfiles.html
title: Font List 
---
<link href='kit.css' rel='stylesheet' type='text/css' nonce="">

{% assign font_files = site.static_files | where: "font", true %}
 {% for myfontfiles in font_files %}
  {% if myfontfiles.extname == '.ttf' %}
<p class='family' style='font-family:"{{ myfontfiles.basename }}"' align='left'>{{ myfontfiles.basename }}</p>
{% endif %}
{% endfor %}

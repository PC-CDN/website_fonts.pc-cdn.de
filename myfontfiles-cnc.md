---
layout: default 
permalink: /myfontfiles-cnc.html
title: Font List 
---
<link href='myfontfiles-cnc.css' rel='stylesheet' type='text/css' nonce="">

{% assign font_files = site.static_files | where: "fontcnc", true %}
 {% for myfontfiles in font_files %}
  {% if myfontfiles.extname == '.ttf' %}
<p class='family' style='font-family:"{{ myfontfiles.basename }}"' align='left'>{{ myfontfiles.basename }}</p>
{% endif %}
{% endfor %}

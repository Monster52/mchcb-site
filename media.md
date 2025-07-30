---
layout: page
title: Media
---

# Photo Gallery

Click images to enlarge.

<div class="gallery">
  {% for image in site.static_files %}
    {% if image.path contains '/assets/images/gallery/' %}
      <a href="{{ image.path | relative_url }}" target="_blank">
        <img src="{{ image.path | relative_url }}" alt="Gallery image">
      </a>
    {% endif %}
  {% endfor %}
</div>

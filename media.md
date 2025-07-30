---
layout: page
title: Media
---

# 📸 Photo Gallery

Click images to enlarge.

<style>
  .gallery {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(240px, 1fr));
    gap: 1rem;
    margin-top: 2rem;
    max-width: 1200px;
    margin-left: auto;
    margin-right: auto;
  }

  .gallery img {
    width: 100%;
    height: auto;
    border-radius: 8px;
    object-fit: cover;
    box-shadow: 0 2px 8px rgba(0,0,0,0.2);
    transition: transform 0.2s ease;
  }

  .gallery img:hover {
    transform: scale(1.05);
  }
</style>

<div class="gallery">
  {% for image in site.static_files %}
    {% if image.path contains '/assets/images/gallery/' %}
      <a href="{{ image.path | relative_url }}" target="_blank">
        <img src="{{ image.path | relative_url }}" alt="Gallery Image">
      </a>
    {% endif %}
  {% endfor %}
</div>

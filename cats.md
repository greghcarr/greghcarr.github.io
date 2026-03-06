---
layout: default
title: Cats
description: Photos of my cats.
---

<style>
h1 { border-bottom: 1px solid #ccc; padding-bottom: 0.2em; width: fit-content; }
.gallery {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(220px, 1fr));
  gap: 12px;
  margin-top: 1em;
}
.gallery figure {
  margin: 0;
}
.gallery img {
  width: 100%;
  height: 220px;
  object-fit: cover;
  border-radius: 6px;
  display: block;
}

</style>

# Cats

<div class="gallery">
  {% assign cat_images = site.static_files | where_exp: "f", "f.path contains '/assets/images/cats/'" %}
  {% for image in cat_images %}
  <figure>
    <img src="{{ image.path }}" alt="{{ image.basename }}">
  </figure>
  {% endfor %}
</div>

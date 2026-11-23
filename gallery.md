---
title: Gallery
permalink: /gallery/
---

# Photo gallery

Every photo placed in the `assets/photos` folder appears here automatically.

<div class="gallery">
{% assign image_exts = ".jpg,.jpeg,.png,.gif,.webp,.JPG,.JPEG,.PNG" | split: "," %}
{% for file in site.static_files %}
  {% if file.path contains "/assets/photos/" and image_exts contains file.extname %}
  <figure>
    <a href="{{ file.path | relative_url }}"><img src="{{ file.path | relative_url }}" alt="{{ file.basename }}" loading="lazy"></a>
    <figcaption>{{ file.basename | replace: "-", " " | replace: "_", " " }}</figcaption>
  </figure>
  {% endif %}
{% endfor %}
</div>

*Tip: name photos descriptively, for example `1965-grandparents-wedding.jpg`. The file name becomes the caption.*

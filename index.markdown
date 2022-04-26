---
layout: page
---

Podpořte prosím spolu se špičkovými fotografy Ukrajinu. Vy pošlete Ukrajincům peníze a fotografové Vám za to vytisknou a zašlou velkoformátovou fotografii. Fotografie pomáhají. [Zjistit více >>](/o-projektu)


{% for photog in site.data.photogs %}
<!-- ## [{{ photog.name }}](/fotografove/{{ photog.slug }}) -->
## {{ photog.name }}
<div class="gallery">
{% assign images = photog.images %}
{% include splide-gallery.html folder="images" %}
</div>
{% endfor %}

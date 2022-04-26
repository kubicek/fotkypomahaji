---
layout: page
---

Podpořte Ukrajinu a získejte fotografii od špičkových autorů

Vyberte si fotografii jednoho z našich profesionálních zpravodajských fotografů, která zachycuje aktuální dění na Ukrajině či humanitární krizi v okolních zemích. Přispějte minimální částkou 2000 Kč na charitu Člověk v tísni, Post Bellum nebo Charita ČR. Pošlete nám potvrzení o platbě a my vám fotografii ve formátu 40x50 cm vytiskneme a zašleme. [Zjistit více >>](/o-projektu)


{% for photog in site.data.photogs %}
## [{{ photog.name }}](/fotografove/{{ photog.slug }})
<div class="gallery">
{% assign images = photog.images %}
{% include splide-gallery.html folder="images" %}
</div>
{% endfor %}

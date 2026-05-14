---
title: "Publications"
layout: gridlay
sitemap: false
permalink: /publications/
---

## Publications

<input type="text" class="pub-search" id="pubSearch" placeholder="Filter by title, author, or year...">

<div class="section-card publication-list" id="pubList" data-pub-searchable>
{% capture publications %}
{% include rivera_publication_list.md %}
{% endcapture %}
{{ publications | markdownify }}
</div>

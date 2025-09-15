---
layout: page
title: Search
permalink: /search/
---

<input id="search-input" type="search" placeholder="Search..." style="width:100%;padding:.6rem 1rem;border:1px solid #ddd;border-radius:8px;">

<ul id="results-container" style="margin-top:1rem;list-style:none;padding-left:0;"></ul>

<!-- CDN 로더 (권장) -->
<script src="https://unpkg.com/simple-jekyll-search@1.11.0/dest/simple-jekyll-search.min.js"></script>


<script>
  SimpleJekyllSearch({
    searchInput: document.getElementById('search-input'),
    resultsContainer: document.getElementById('results-container'),
    json: '{{ '/search.json' | relative_url }}',
    searchResultTemplate:
      '<li style="margin:.5rem 0;"><a href="{url}">{title}</a> <small style="color:#888;">{date}</small></li>',
    noResultsText: 'No results',
    fuzzy: true,
    limit: 20
  });
</script>

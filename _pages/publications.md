---
layout: page
permalink: /publications/
title: Publications
description:
nav: true
nav_order: 2
---

<!-- _pages/publications.md -->

<div class="pub-type-filter" style="margin-bottom: 1rem">
  <label style="margin-right: 1.5rem; cursor: pointer">
    <input type="checkbox" id="pub-filter-journal" checked style="margin-right: 0.4rem" />
    Journal
  </label>
  <label style="cursor: pointer">
    <input type="checkbox" id="pub-filter-communications" checked style="margin-right: 0.4rem" />
    Communications
  </label>
</div>

<div class="publications">

{% bibliography %}

</div>

<script>
  (function () {
    function applyFilter() {
      var journalOn = document.getElementById('pub-filter-journal').checked;
      var commOn = document.getElementById('pub-filter-communications').checked;
      var container = document.querySelector('.publications');
      if (!container) return;
      var currentHeading = null;
      Array.prototype.forEach.call(container.children, function (child) {
        var tag = child.tagName;
        if (tag === 'H2' || tag === 'H3' || tag === 'H4' || tag === 'H5') {
          currentHeading = child;
          return;
        }
        if (tag === 'OL') {
          var anyVisible = false;
          Array.prototype.forEach.call(child.querySelectorAll('li'), function (li) {
            var typeEl = li.querySelector('[data-pub-type]');
            var type = typeEl ? typeEl.getAttribute('data-pub-type') : '';
            var show = type === 'article' ? journalOn : commOn;
            li.style.display = show ? '' : 'none';
            if (show) anyVisible = true;
          });
          child.style.display = anyVisible ? '' : 'none';
          if (currentHeading) currentHeading.style.display = anyVisible ? '' : 'none';
        }
      });
    }
    var journalBox = document.getElementById('pub-filter-journal');
    var commBox = document.getElementById('pub-filter-communications');
    if (journalBox) journalBox.addEventListener('change', applyFilter);
    if (commBox) commBox.addEventListener('change', applyFilter);
    applyFilter();
  })();
</script>

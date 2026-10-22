---
layout: page
title: cv
permalink: /cv/
nav: true
nav_order: 1.5
---

{% assign cv = site.data.socials.cv_pdf | relative_url %}

<p><a href="{{ cv }}" target="_blank" rel="noopener"><i class="fa-solid fa-file-pdf"></i> Download my CV (PDF)</a></p>

<object data="{{ cv }}" type="application/pdf" width="100%" style="height: 85vh; border: 1px solid var(--global-divider-color); border-radius: 0.5rem;">
  <p>Your browser can't display the PDF here. <a href="{{ cv }}">Download the CV</a> instead.</p>
</object>

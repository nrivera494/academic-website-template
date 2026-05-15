---
title: "About"
layout: gridlay
sitemap: false
permalink: /about/
---

## About

<div class="section-card">
<div class="pi-card">
<img src="{{ site.url }}{{ site.baseurl }}/images/{{ site.photo }}" class="pi-photo" alt="{{ site.name }}" loading="eager">
<div>
<h3 class="pi-name">{{ site.name }}</h3>
<p style="font-style: italic; color: var(--text-secondary);">{{ site.title }}, {{ site.institution }}</p>
<div class="pi-links">
{% if site.email %}<a href="mailto:{{ site.email }}" class="icon-link" title="Email"><i class="fa-solid fa-envelope"></i></a>{% endif %}
{% if site.links.cv and site.links.cv != "" %}
  {% if site.links.cv contains "http" %}
  <a href="{{ site.links.cv }}" class="icon-link" title="CV"><i class="ai ai-cv"></i></a>
  {% else %}
  <a href="{{ site.url }}{{ site.baseurl }}/{{ site.links.cv }}" class="icon-link" title="CV"><i class="ai ai-cv"></i></a>
  {% endif %}
{% endif %}
{% if site.links.google_scholar and site.links.google_scholar != "" %}<a href="{{ site.links.google_scholar }}" class="icon-link" title="Google Scholar"><i class="ai ai-google-scholar"></i></a>{% endif %}
{% if site.links.github and site.links.github != "" %}<a href="{{ site.links.github }}" class="icon-link" title="GitHub"><i class="fa-brands fa-github"></i></a>{% endif %}
{% if site.links.researchgate and site.links.researchgate != "" %}<a href="{{ site.links.researchgate }}" class="icon-link" title="ResearchGate"><i class="ai ai-researchgate"></i></a>{% endif %}
{% if site.links.linkedin and site.links.linkedin != "" %}<a href="{{ site.links.linkedin }}" class="icon-link" title="LinkedIn"><i class="fa-brands fa-linkedin"></i></a>{% endif %}
{% if site.links.twitter and site.links.twitter != "" %}<a href="{{ site.links.twitter }}" class="icon-link" title="X"><i class="fa-brands fa-x-twitter"></i></a>{% endif %}
</div>
{% if site.data.pi[0].education %}
<ul style="margin-top: var(--space-4);">
{% for education in site.data.pi[0].education %}
<li>{{ education | replace: "-","&#8211;" }}</li>
{% endfor %}
</ul>
{% endif %}
</div>
</div>
</div>

<div class="section-card">
<h3>Bio</h3>
<p>I am currently an Assistant Professor in the <a href="https://www.aep.cornell.edu/aep">School of Applied and Engineering Physics</a> at Cornell University. From 2022-2025, I was a postdoc at Harvard, funded by a Junior Fellowship from the <a href="https://socfell.fas.harvard.edu/about">Harvard Society of Fellows</a>. There, I worked on various problems of quantum and nonlinear optics. I completed my PhD in the Physics department at the Massachusetts Institute of Technology (2016-2022), as a <a href="https://www.krellinst.org/csgf/">Computational Science Graduate Fellow</a> of the US Department of Energy (2016-2020) and a Dean's Fellow of the MIT School of Science (2020-2022). For my thesis work, I was awarded the <a href="https://physics.mit.edu/academic-programs/student-awards/">Andrew M. Lockett III Memorial Prize</a>. My primary thesis supervisor was <a href="https://www.rle.mit.edu/marin/">Prof. Marin Soljacic</a>, but I have also worked closely with <a href="https://physics.mit.edu/faculty/john-joannopoulos/">Prof. John Joannopoulos</a> (MIT) and <a href="https://kaminer.technion.ac.il/">Prof. Ido Kaminer</a> (Technion), as well as many others. In 2016, I received my Bachelor's degree in Physics from the Massachusetts Institute of Technology (2012-2016). For my bachelor's thesis, I received the <a href="https://www.aps.org/programs/honors/prizes/apker.cfm">LeRoy Apker Award</a> of the American Physical Society.</p>
</div>

{% if site.data.grants.size > 0 %}
<div class="section-card">
<h3>Grants</h3>
<ul>
{% for grant in site.data.grants %}
<li>{{ grant.name }}</li>
{% endfor %}
</ul>
</div>
{% endif %}

{% if site.data.awards.size > 0 %}
<div class="section-card">
<h3>Awards</h3>
<ul>
{% for award in site.data.awards %}
<li>{{ award.name | replace: "-","&#8211;" }}</li>
{% endfor %}
</ul>
</div>
{% endif %}

{% if site.data.people.size > 0 %}
<div class="section-card">
<h3>Students and Mentoring</h3>
<ul>
{% for student in site.data.people %}
<li>{{ student.name }}, {{ student.location }} ({{ student.degree }}, {{ student.year }})</li>
{% endfor %}
</ul>
</div>
{% endif %}

{% if site.data.funders.size > 0 %}
<div class="section-card">
<h4>Sponsors</h4>
<div class="sponsor-logos" style="display: flex; flex-wrap: wrap; align-items: center; justify-content: center; gap: var(--space-6);">
{% for funder in site.data.funders %}
<a href="{{ funder.url }}" target="_blank"><img src="{{ site.url }}{{ site.baseurl }}/images/{{ funder.image }}" alt="Funder logo" style="max-height: 80px; max-width: 200px; border-radius: 0;" loading="lazy"></a>
{% endfor %}
</div>
</div>
{% endif %}

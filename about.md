---
layout: default
title: About
permalink: "/about"
description: The person behind the medicine, code, music, and writing.
---
<div class="about-journal site-shell">
  <section class="about-intro" aria-labelledby="about-title">
    <div><p class="eyebrow"><span class="hello-dot"></span> The person behind the tabs</p><h1 id="about-title">A few different hats.<br><em>Still just me.</em><span class="sunburst" aria-hidden="true">✳</span></h1><p class="about-lead">I’m {{ site.author.name }} — a medical doctor, solutions architect, and musician based in {{ site.author.location }}.</p><p>I like making useful things, figuring things out, and following an interesting idea a little further than I probably should.</p><p>Medicine, software, music, writing. It all finds a home here. {{ site.author.bio_short }}</p><a class="journal-button" href="mailto:{{ site.author.email }}">Say hello <span aria-hidden="true">↗</span></a></div>
    <figure class="about-portrait"><img src="{{ site.author.about_photo | relative_url }}" alt="Tanaka Mawere smiling" width="3264" height="2448" fetchpriority="high"><figcaption class="photo-scribble">a face to all those interests :)</figcaption></figure>
  </section>
  <section class="about-chapters" aria-labelledby="chapters-title"><div class="section-heading"><div><p class="eyebrow">Same person. Different worlds.</p><h2 id="chapters-title">The things I keep coming <em>back to.</em></h2></div></div>
    <div class="about-chapter-grid">
      <article class="about-chapter"><img src="{{ '/assets/img/dev_fest.png' | relative_url }}" alt="Tanaka at a developer event" loading="lazy" width="640" height="440"><div><p class="eyebrow">01 / Building</p><h3>Code & curiosity</h3><p>Started with Python (like everyone else), moved to Java for Android, and settled on C# and .NET for everything.</p><a class="journal-text-link" href="{{ '/projects/' | relative_url }}">Things I’m building <span aria-hidden="true">↗</span></a></div></article>
      <article class="about-chapter"><img src="{{ '/assets/img/me_medicine.jpg' | relative_url }}" alt="Tanaka in medical attire" loading="lazy" width="640" height="440"><div><p class="eyebrow">02 / Medicine</p><h3>People come first</h3><p>I am a doctor now! I’m especially interested in where healthcare and technology meet, and how useful software can support the work of caring for people.</p><a class="journal-text-link" href="{{ '/projects/medbase' | relative_url }}">Explore Medbase <span aria-hidden="true">↗</span></a></div></article>
      <article class="about-chapter"><img src="{{ '/assets/img/music2.jpg' | relative_url }}" alt="Tanaka making music" loading="lazy" width="640" height="440"><div><p class="eyebrow">03 / Music</p><h3>A little rhythm</h3><p>I play keyboard and bass. I then pretend to know what I’m doing on the drums, acoustic guitar, marimba, and in singing.</p><span class="photo-scribble">always room for another instrument</span></div></article>
    </div>
  </section>
  <section class="about-footnote"><div><p class="eyebrow">A few tools in the bag</p><h2>Different skills.<br><em>Shared curiosity.</em></h2></div><div><div class="skill-notes">{% for skill in site.author.skills %}<span>{{ skill }}</span>{% endfor %}</div><p>I also write about faith, health, technology, and the little things I notice along the way.</p><a class="journal-text-link" href="{{ '/posts/' | relative_url }}">Step into the notebook <span aria-hidden="true">→</span></a></div></section>
  <section class="projects-contact"><div><p class="eyebrow">Keep the conversation going</p><h2>Good to <em>meet you.</em></h2></div><a class="journal-button" href="mailto:{{ site.author.email }}">Let’s talk <span aria-hidden="true">↗</span></a></section>
</div>

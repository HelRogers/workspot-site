---
layout: layouts/base.njk
title: Ventures
permalink: /ventures/
description: The businesses and projects that sit under WorkSpot Ltd.
---

<section class="hero">
  <div class="container">
    <span class="eyebrow">Ventures</span>
    <h1>What WorkSpot does, in practice<span class="accent" aria-hidden="true"></span></h1>
    <p class="lede" style="margin-top: 2rem; max-width: 56ch;">Three businesses sit under the WorkSpot roof today. Each one stands on its own, with its own clients, customers and remit. What they share is the way the work gets done.</p>
  </div>
</section>

<section style="border-top: 1px solid var(--rule); padding-top: 3rem;">
  <div class="container">
    <div class="ventures">
      {% for venture in ventures %}
      <article class="venture">
        <div class="venture-number">0{{ loop.index }}</div>
        <h3>{{ venture.name }}</h3>
        {% if venture.subtitle %}<p class="venture-subtitle">{{ venture.subtitle }}</p>{% endif %}
        <p class="tagline">{{ venture.tagline }}</p>
        <p>{{ venture.description }}</p>
        {% if venture.partner %}
        <p class="venture-partner">In partnership with <a href="{{ venture.partnerUrl }}" target="_blank" rel="noopener">{{ venture.partner }}</a></p>
        {% endif %}
        <div class="venture-foot">
          <span class="venture-status {% if venture.status == 'In progress' or venture.status == 'Coming soon' %}coming{% endif %}">{{ venture.status }}</span>
          {% if venture.url and venture.url != "#" %}
          <a href="{{ venture.url }}" class="venture-link" target="_blank" rel="noopener">Visit →</a>
          {% endif %}
        </div>
      </article>
      {% endfor %}
    </div>
  </div>
</section>

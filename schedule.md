---
layout: default
title: Schedule
permalink: /schedule/
---
<section class="section">
  <div class="wrap">
    <div class="section-head">
      <div class="eyebrow">{{ site.team.age_division }} Schedule</div>
      <h2>Summer 2026 Tournaments</h2>
      <p>
        Tournaments the team has played in and will play in this summer.
        Follow along on GameChanger for live scoring and results.
      </p>
    </div>

    <div class="tournament-grid">
      {% for t in site.data.schedule %}
      <div class="tournament-card">
        <div class="logo-wrap">
          {% if t.logo %}
            <img src="{{ t.logo | relative_url }}" alt="{{ t.name }} logo">
          {% else %}
            <div class="placeholder">{{ t.name }}</div>
          {% endif %}
        </div>
        <div class="card-body">
          <h3>{{ t.name }}</h3>
          <div class="dates">{{ t.dates }}</div>
          <div class="loc">
            {{ t.location_name }}
            {% if t.address %}<span class="addr">{{ t.address }}</span>{% endif %}
          </div>
          {% if t.link %}<a class="site-link" href="{{ t.link }}" target="_blank" rel="noopener">Tournament Website &rarr;</a>{% endif %}
        </div>
      </div>
      {% endfor %}
    </div>
  </div>
</section>

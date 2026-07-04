---
layout: default
title: Schedule
permalink: /schedule/
---
<section class="section">
  <div class="wrap">
    <div class="section-head">
      <div class="eyebrow">{{ site.team.age_division }} Schedule</div>
      <h2>Tournaments &amp; Showcases</h2>
      <p>
        Game times and fields are subject to change based on tournament brackets and weather.
        Check back for updates, or follow the team on GameChanger for live scoring.
      </p>
    </div>

    {% for t in site.data.schedule %}
    <div class="tournament">
      <div class="tournament-head">
        <h2>{{ t.name }}</h2>
        <div class="loc">{{ t.location_name }}{% if t.address %} &middot; {{ t.address }}{% endif %}</div>
        <div class="dates">{{ t.dates }}</div>
      </div>
      <div class="game-list">
        {% for g in t.games %}
        <div class="game-row">
          <div class="when">
            <span class="d">{{ g.date }}</span>
            <span class="t">{{ g.time }}</span>
          </div>
          <div>
            <div class="opp">{{ g.opponent }}</div>
            {% if g.field %}<span class="field">{{ g.field }}</span>{% endif %}
          </div>
          <div class="result">{{ g.result }}</div>
        </div>
        {% endfor %}
      </div>
    </div>
    {% endfor %}
  </div>
</section>

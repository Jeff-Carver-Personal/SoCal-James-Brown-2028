---
layout: default
title: Roster
permalink: /roster/
---
<section class="section">
  <div class="wrap">
    <div class="section-head">
      <div class="eyebrow">Roster</div>
      <h2>{{ site.team.name }}</h2>
      <p>Tap any player to view her full profile, including academics, position, and measurables.</p>
    </div>

    <div class="roster-grid">
      {% assign sorted_players = site.players | sort: "number" %}
      {% for player in sorted_players %}
      <a class="player-card" href="{{ player.url | relative_url }}">
        <div class="photo-wrap">
          {% if player.photo %}
            <img src="{{ player.photo | relative_url }}" alt="{{ player.name }}" loading="lazy">
          {% else %}
            <div class="placeholder">{{ player.number }}</div>
          {% endif %}
          <div class="grad-year">'{{ player.grad_year | slice: 2, 2 }}</div>
          <div class="num-pennant"><span class="pennant">#{{ player.number }}</span></div>
        </div>
        <div class="card-body">
          <h3>{{ player.name }}</h3>
          <div class="meta">{{ player.hometown }}</div>
          <div class="meta">{{ player.high_school }}</div>
          <div class="meta">GPA: {{ player.gpa }}</div>
          <span class="pos-tag">{{ player.position }}</span>
        </div>
      </a>
      {% endfor %}
    </div>
  </div>
</section>

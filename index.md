---
layout: default
title: Home
---
<section class="hero">
  <img class="hero-photo" src="{{ '/assets/images/team-photo.jpg' | relative_url }}" alt="So Cal Athletics James/Brown 28 Premier team photo">
  <div class="hero-scrim"></div>
  <div class="hero-content wrap">
    <div class="eyebrow">{{ site.team.age_division }} Travel Softball &middot; Est. Roster</div>
    <h1 class="hero-title">{{ site.team.name }}</h1>
    <div class="hero-sub">Building on every rep, every rotation, every road trip.</div>
    <div class="hero-actions">
      <a class="btn solid" href="{{ '/roster/' | relative_url }}">Meet the Team</a>
      <a class="btn" href="{{ '/schedule/' | relative_url }}">Tournament Schedule</a>
    </div>
  </div>
</section>

<section class="section">
  <div class="wrap">
    <div class="section-head">
      <div class="eyebrow">About the Team</div>
      <h2>Who We Are</h2>
      <p>
        So Cal Athletics James/Brown 28 Premier is a {{ site.team.age_division }} travel softball team
        built around fundamentals, competition, and college exposure. The team travels to
        showcases and tournaments throughout the season, competing against top programs from
        across the region.
      </p>
    </div>
    <div class="about-grid">
      <div class="stat-card">
        <div class="num">{{ site.players | size }}</div>
        <div class="label">Players on Roster</div>
      </div>
      <div class="stat-card">
        <div class="num">{{ site.team.age_division }}</div>
        <div class="label">Age Division</div>
      </div>
      <div class="stat-card">
        <div class="num">2028</div>
        <div class="label">Primary Grad Class</div>
      </div>
    </div>
  </div>
</section>

<section class="section dark">
  <div class="wrap">
    <div class="section-head">
      <div class="eyebrow">Leadership</div>
      <h2>Coaching Staff</h2>
    </div>
    <div class="coach-grid">
      <div class="coach-card">
        <div class="role">Head Coach</div>
        <div class="name">{{ site.team.head_coach }}</div>
        <div class="phone">{{ site.team.head_coach_phone }}</div>
      </div>
      <div class="coach-card">
        <div class="role">Assistant Coach</div>
        <div class="name">{{ site.team.assistant_coach }}</div>
        <div class="phone">{{ site.team.assistant_coach_phone }}</div>
      </div>
      <div class="coach-card">
        <div class="role">Recruiting Coordinator</div>
        <div class="name">{{ site.team.recruiting_coordinator }}</div>
        <div class="phone">{{ site.team.recruiting_coordinator_phone }}</div>
      </div>
    </div>
  </div>
</section>

<section class="section">
  <div class="wrap" style="text-align:center;">
    <div class="eyebrow">Stay Connected</div>
    <h2>Follow Along</h2>
    <p style="color:var(--ink-soft); max-width:520px; margin: 0 auto 8px;">
      Follow the team on social media and GameChanger for live updates, scores, and highlights.
    </p>
  </div>
</section>

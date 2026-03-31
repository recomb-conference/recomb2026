---
layout: page
title: Program
---

<style>
  .program-legacy {
    --program-ink: #282555;
    --program-muted: #66708f;
    --program-accent: #3d3a6e;
    --program-accent-soft: #eef1fb;
    --program-line: #d7dced;
    --program-panel: #ffffff;
    --program-break-bg: #f4f6fb;
    --program-break-ink: #1f1f1f;
    --program-keynote-bg: #fff4f1;
    --program-keynote-ink: #99342c;
    --program-poster-bg: #f5f1fb;
    --program-poster-ink: #5c3d87;
    --program-social-bg: #fbf4e8;
    --program-social-ink: #7a5422;
    max-width: 600px;
    margin: 0 auto;
    padding: 0 8px 10px;
  }

  .program-legacy .program-legacy-header {
    text-align: center;
    margin: 0 0 32px;
  }

  .program-legacy .program-legacy-header hr {
    border: 0;
    border-top: 1px solid #bfc6df;
    margin: 0 0 18px;
  }

  .program-legacy .program-legacy-header h2 {
    margin: 0;
    font-family: "Merriweather", serif;
    font-size: 1.8rem;
    font-weight: 700;
    color: var(--program-ink);
    letter-spacing: 0.02em;
  }

  .program-legacy .program-day {
    margin-bottom: 34px;
  }

  .program-legacy .program-day-title {
    margin: 0 0 12px;
    font-family: "Lato", sans-serif;
    font-size: 1.18rem;
    font-weight: 700;
    color: var(--program-ink);
    text-align: center;
  }

  .program-legacy .program-day-rule {
    height: 2px;
    border: 0;
    background: linear-gradient(90deg, var(--program-accent) 0%, rgba(61, 58, 110, 0.2) 100%);
    max-width: 760px;
    margin: 0 auto 14px;
  }

  .program-legacy .program-list,
  .program-legacy .track-panel {
    background: var(--program-panel);
    border-top: 2px solid var(--program-line);
    border-bottom: 2px solid var(--program-line);
    border-left: 0;
    border-right: 0;
    box-shadow: none;
  }

  .program-legacy .program-list {
    max-width: 760px;
    margin: 0 auto;
  }

  .program-legacy .program-row {
    display: block;
  }

  .program-legacy .program-row + .program-row {
    border-top: 2px solid var(--program-line);
  }

  .program-legacy .program-item {
    padding: 14px 18px;
    background: transparent;
    color: var(--program-ink);
    font-family: "Open Sans", sans-serif;
    font-size: 0.98rem;
    font-weight: 600;
    line-height: 1.45;
    text-align: center;
    box-sizing: border-box;
  }

  .program-legacy .session-row .program-item {
    background: #48688F;
    color: #ffffff;
  }

  .program-legacy .session-row .program-item,
  .program-legacy .keynote-row .program-item,
  .program-legacy .poster-row .program-item,
  .program-legacy .social-row .program-item {
    display: block;
    width: 100%;
    max-width: none;
    margin: 7px;
    padding: 11px 28px;
    border-radius: 0;
    box-shadow: none;
  }

  .program-legacy .break-row .program-item {
    background: transparent;
    color: var(--program-break-ink);
    padding: 12px 18px;
  }

  .program-legacy .break-row .program-item {
    font-weight: 700;
  }

  .program-legacy .keynote-row .program-item {
    background: var(--program-keynote-bg);
    color: var(--program-keynote-ink);
  }

  .program-legacy .poster-row .program-item {
    background: var(--program-poster-bg);
    color: var(--program-poster-ink);
  }

  .program-legacy .social-row .program-item {
    background: var(--program-social-bg);
    color: var(--program-social-ink);
  }

  .program-legacy .closing-row .program-item {
    background: #1f2449;
    color: #ffffff;
  }

  .program-legacy .buffer-row .program-item {
    background: #eef1f6;
    color: var(--program-ink);
  }

  .program-legacy .parallel-grid {
    display: grid;
    grid-template-columns: repeat(2, minmax(0, 1fr));
    gap: 0;
    max-width: 760px;
    margin: 0 auto;
    border-top: 2px solid var(--program-line);
    border-bottom: 2px solid var(--program-line);
    border-left: 0;
    border-right: 0;
    background: var(--program-panel);
    box-shadow: none;
  }

  .program-legacy .track-panel {
    overflow: hidden;
    max-width: none;
    margin: 0;
    border: 0;
    box-shadow: none;
  }

  .program-legacy .track-panel + .track-panel {
    border-left: 0;
  }

  .program-legacy .track-title {
    margin: 0;
    padding: 14px 18px;
    background: var(--program-accent);
    color: #ffffff !important;
    font-size: 0.82rem;
    font-weight: 700;
    letter-spacing: 0.16em;
    text-transform: uppercase;
    text-align: center;
  }

  .program-legacy .track-panel .program-list {
    border: 0;
    box-shadow: none;
    max-width: none;
  }

  .program-legacy .program-links {
    display: grid;
    grid-template-columns: repeat(2, minmax(0, 1fr));
    gap: 16px;
    max-width: 760px;
    margin: 8px auto 0;
  }

  .program-legacy .program-link {
    display: block;
    padding: 16px 18px;
    border: 1px solid var(--program-line);
    background: #f9fafc;
    color: var(--program-ink);
    font-family: "Lato", sans-serif;
    font-weight: 700;
    text-align: center;
    text-decoration: none;
    box-shadow: 0 10px 24px rgba(25, 34, 74, 0.05);
  }

  .program-legacy .program-link:hover {
    background: var(--program-accent-soft);
    color: var(--program-ink);
  }

  @media screen and (max-width: 799px) {
    .program-legacy {
      padding: 0;
    }

    .program-legacy .parallel-grid,
    .program-legacy .program-links {
      grid-template-columns: 1fr;
    }

    .program-legacy .parallel-grid {
      border: 0;
      background: transparent;
      box-shadow: none;
      gap: 18px;
    }

    .program-legacy .track-panel {
      border: 1px solid var(--program-line);
      box-shadow: 0 12px 30px rgba(25, 34, 74, 0.07);
    }

    .program-legacy .track-panel + .track-panel {
      border-left: 1px solid var(--program-line);
    }

    .program-legacy .program-item {
      padding: 12px 16px 14px;
    }

    .program-legacy .program-legacy-header h2 {
      font-size: 1.45rem;
    }

    .program-legacy .program-day-title {
      font-size: 1.05rem;
    }
  }
</style>

<section class="program-legacy">

  <section class="program-day">
    <h3 class="program-day-title">Day 1 — Tuesday, May 26 (09:00 - 19:15)</h3>
    <hr class="program-day-rule">

    <div class="program-list">
      <div class="program-row">
        <div class="program-item"><strong>Welcome</strong></div>
      </div>

      <div class="program-row keynote-row">
        <div class="program-item">Keynote 1</div>
      </div>

      <div class="program-row break-row">
        <div class="program-item">Coffee Break I</div>
      </div>

      <div class="program-row session-row">
        <div class="program-item">Session</div>
      </div>

      <div class="program-row break-row">
        <div class="program-item">Lunch Break</div>
      </div>

      <div class="program-row session-row">
        <div class="program-item">Session</div>
      </div>

      <div class="program-row break-row">
        <div class="program-item">Coffee Break II</div>
      </div>

      <div class="program-row session-row">
        <div class="program-item">Session</div>
      </div>

      <div class="program-row poster-row">
        <div class="program-item">Poster Session I</div>
      </div>
    </div>
  </section>

  <section class="program-day">
    <h3 class="program-day-title">Day 2 — Wednesday, May 27 (09:00 - 19:15)</h3>
    <hr class="program-day-rule">

    <div class="parallel-grid">
      <div class="track-panel">
        <h4 class="track-title">Main Track</h4>

        <div class="program-list">
          <div class="program-row">
            <div class="program-item"><strong>Welcome</strong></div>
          </div>

          <div class="program-row keynote-row">
            <div class="program-item">Keynote 2</div>
          </div>

          <div class="program-row break-row">
            <div class="program-item">Coffee Break I</div>
          </div>

          <div class="program-row session-row">
            <div class="program-item">Session</div>
          </div>

          <div class="program-row break-row">
            <div class="program-item">Lunch Break</div>
          </div>

          <div class="program-row session-row">
            <div class="program-item">Session</div>
          </div>

          <div class="program-row break-row">
            <div class="program-item">Coffee Break II</div>
          </div>

          <div class="program-row session-row">
            <div class="program-item">Session</div>
          </div>

          <div class="program-row poster-row">
            <div class="program-item">Poster Session II</div>
          </div>
        </div>
      </div>

      <div class="track-panel">
        <h4 class="track-title">Parallel Track</h4>

        <div class="program-list">
          <div class="program-row">
            <div class="program-item"><strong>Welcome</strong></div>
          </div>

          <div class="program-row session-row">
            <div class="program-item">Session</div>
          </div>

          <div class="program-row break-row">
            <div class="program-item">Lunch Break</div>
          </div>

          <div class="program-row session-row">
            <div class="program-item">Session</div>
          </div>

          <div class="program-row break-row">
            <div class="program-item">-</div>
          </div>

          <div class="program-row break-row">
            <div class="program-item">-</div>
          </div>

          <div class="program-row break-row">
            <div class="program-item">-</div>
          </div>

          <div class="program-row break-row">
            <div class="program-item">-</div>
          </div>

          <div class="program-row break-row">
            <div class="program-item">-</div>
          </div>
        </div>
      </div>
    </div>
  </section>

  <section class="program-day">
    <h3 class="program-day-title">Day 3 — Thursday, May 28 (09:00 - 17:40)</h3>
    <hr class="program-day-rule">

    <div class="program-list">
      <div class="program-row">
        <div class="program-item"><strong>Welcome</strong></div>
      </div>

      <div class="program-row keynote-row">
        <div class="program-item">Keynote 3</div>
      </div>

      <div class="program-row break-row">
        <div class="program-item">Coffee Break I</div>
      </div>

      <div class="program-row session-row">
        <div class="program-item">Session</div>
      </div>

      <div class="program-row break-row">
        <div class="program-item">Lunch Break</div>
      </div>

      <div class="program-row keynote-row">
        <div class="program-item">Keynote 4</div>
      </div>

      <div class="program-row session-row">
        <div class="program-item">Session</div>
      </div>

      <div class="program-row break-row">
        <div class="program-item">Coffee Break II</div>
      </div>

      <div class="program-row session-row">
        <div class="program-item">Session</div>
      </div>

      <div class="program-row">
        <div class="program-item">Business Meeting</div>
      </div>

      <div class="program-row social-row">
        <div class="program-item">Gala Dinner</div>
      </div>
    </div>
  </section>

  <section class="program-day">
    <h3 class="program-day-title">Day 4 — Friday, May 29 (09:00 - 18:15)</h3>
    <hr class="program-day-rule">

    <div class="program-list">
      <div class="program-row">
        <div class="program-item"><strong>Welcome</strong></div>
      </div>

      <div class="program-row keynote-row">
        <div class="program-item">Keynote 5</div>
      </div>

      <div class="program-row break-row">
        <div class="program-item">Coffee Break I</div>
      </div>

      <div class="program-row session-row">
        <div class="program-item">Session</div>
      </div>

      <div class="program-row break-row">
        <div class="program-item">Lunch Break</div>
      </div>

      <div class="program-row session-row">
        <div class="program-item">Session</div>
      </div>

      <div class="program-row break-row">
        <div class="program-item">Coffee Break II</div>
      </div>

      <div class="program-row session-row">
        <div class="program-item">Session</div>
      </div>

      <div class="program-row buffer-row">
        <div class="program-item">Session (buffer)</div>
      </div>

      <div class="program-row closing-row">
        <div class="program-item">Closing Session and Awards</div>
      </div>
    </div>
  </section>

  <div class="program-links">
    <a class="program-link" href="{{ '/accepted_papers.md' | relative_url }}">RECOMB 2026: List of Accepted Papers</a>
    <a class="program-link" href="https://recomb.org/proceedings/proceedings/2030-2026/2026/">RECOMB 2026 Proceedings</a>
  </div>
</section>

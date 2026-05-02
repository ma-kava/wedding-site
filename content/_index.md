---
title: " "
bigimg: [{src: "/img/razanac.jpg", desc: "Těšíme se na vás!"}]
---

<style>
@import url('https://fonts.googleapis.com/css2?family=Playfair+Display:ital,wght@0,400;0,600;0,700;1,400&family=Lora:ital,wght@0,400;0,500;1,400&display=swap');

html {
  scroll-behavior: smooth;
}

/* ── Mist fade-in ── */
@keyframes mistFadeIn {
  0% { opacity: 0; transform: translateY(30px); }
  100% { opacity: 1; transform: translateY(0); }
}

/* ── Card base ── */
.card-base {
  background: #39472f;
  border-radius: 14px;
  position: relative;
  box-shadow:
    0 6px 0 #20291a,
    0 16px 30px rgba(0,0,0,0.3);
  border: 1px solid rgba(223, 205, 182, 0.15);
  animation: mistFadeIn 1s ease-out forwards;
  opacity: 0;
  transition: transform 0.35s ease, box-shadow 0.35s ease;
}

.card-base:hover {
  transform: translateY(-4px);
  box-shadow:
    0 10px 0 #20291a,
    0 22px 40px rgba(0,0,0,0.4);
}

/* ── Verse card ── */
.verse-card {
  max-width: 720px;
  margin: 0 auto 3em auto;
  padding: 2.5em 3em;
  background: linear-gradient(135deg, #425237 0%, #324029 100%);
  border-left: 3px solid #b35a41;
  border-right: 3px solid #b35a41;
  box-shadow:
    0 6px 0 #20291a,
    0 16px 30px rgba(0,0,0,0.3);
}

/* ── Three-column card grid ── */
.cards-grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 1.5em;
  max-width: 1050px;
  margin: 0 auto 3em auto;
}

.cards-grid .card-base {
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  padding: 2.2em 2em;
  min-height: 260px;
}

/* ── RSVP highlight card ── */
.rsvp-highlight {
  background: linear-gradient(135deg, #b35a41 0%, #964a34 100%);
  border: none;
}
.rsvp-highlight .card-heading,
.rsvp-highlight .card-text {
  color: #ffffff !important;
}
.rsvp-highlight .card-icon {
  background: rgba(255,255,255,0.2);
  border-color: rgba(255,255,255,0.4);
}
.rsvp-highlight .card-icon--ring::after {
  border-color: #ffffff;
}

/* ── Form Transition Background ── */
.form-transition-wrapper {
  margin: 4em auto; /* Centered */
  padding: 1em 15px;
}

/* ── RSVP form card ── */
.form-card {
  background: transparent !important;
  max-width: 800px;
  margin: 0 auto;
  padding: 3em 1em 1em 1em;
  border: none;
  border-radius: 16px;
  animation-delay: 0.3s;
}
.form-card:hover {
  transform: none;
  box-shadow: 0 20px 50px rgba(0,0,0,0.2);
}

/* ── Button ── */
.custom-btn {
  background: linear-gradient(135deg, #b6c8c2 0%, #87a398 100%);
  border: none;
  border-radius: 6px;
  padding: 0.7em 2em;
  font-weight: 600;
  font-family: 'Lora', 'Georgia', serif;
  letter-spacing: 0.04em;
  color: #2d3a24 !important;
  transition: all 0.3s ease;
  text-decoration: none !important;
  display: inline-block;
  box-shadow: 0 3px 10px rgba(0,0,0,0.2);
  font-size: 0.95em;
  text-transform: uppercase;
}
.custom-btn:hover {
  background: linear-gradient(135deg, #dfcdb6 0%, #c4a98a 100%);
  transform: translateY(-2px);
  box-shadow: 0 5px 16px rgba(0,0,0,0.3);
  color: #1f2a18 !important;
  text-decoration: none !important;
}

.rsvp-highlight .custom-btn {
  background: #ffffff;
  color: #b35a41 !important;
}
.rsvp-highlight .custom-btn:hover {
  background: #dfcdb6;
  color: #964a34 !important;
}

/* ── Card headings ── */
.card-heading {
  font-family: 'Playfair Display', 'Georgia', serif;
  color: #e5a983;
  margin-bottom: 0.7em;
  font-size: 1.35em;
  font-weight: 600;
  letter-spacing: 0.01em;
  display: flex;
  align-items: center;
  gap: 10px;
}

.card-text {
  font-family: 'Lora', 'Georgia', serif;
  font-size: 1.05em;
  color: #dfcdb6;
  line-height: 1.7;
}

/* ── CSS Decorative icons for card headings ── */
.card-icon {
  display: inline-flex;
  align-items: center;
  justify-content: center;
  width: 32px;
  height: 32px;
  border-radius: 50%;
  background: rgba(223, 205, 182, 0.1);
  border: 1px solid rgba(223, 205, 182, 0.3);
  flex-shrink: 0;
}

/* Ring icon */
.card-icon--ring::after {
  content: '';
  width: 12px;
  height: 12px;
  border: 2px solid #dfcdb6;
  border-radius: 50%;
}

/* Calendar icon */
.card-icon--cal {
  position: relative;
}
.card-icon--cal::before {
  content: '';
  width: 12px;
  height: 13px;
  border: 1.5px solid #dfcdb6;
  border-radius: 2px;
  position: absolute;
}
.card-icon--cal::after {
  content: '25';
  font-size: 7px;
  font-weight: 700;
  color: #dfcdb6;
  margin-top: 3px;
  font-family: 'Lora', sans-serif;
}

/* Music / timeline icon */
.card-icon--timeline {
  position: relative;
}
.card-icon--timeline::before {
  content: '';
  width: 2px;
  height: 14px;
  background: #dfcdb6;
  position: absolute;
  left: 50%;
  transform: translateX(-50%);
}
.card-icon--timeline::after {
  content: '';
  width: 6px;
  height: 6px;
  border-radius: 50%;
  background: #dfcdb6;
  position: absolute;
  top: 5px;
  left: 50%;
  transform: translateX(-50%);
}

/* ── Decorative line divider ── */
.section-divider {
  text-align: center;
  margin: 3em auto;
  max-width: 300px;
  border: none;
  height: 1px;
  background: linear-gradient(90deg, transparent 0%, rgba(223, 205, 182, 0.3) 30%, rgba(223, 205, 182, 0.6) 50%, rgba(223, 205, 182, 0.3) 70%, transparent 100%);
}

/* ── Leaf ornament for verse card ── */
.leaf-ornament {
  position: absolute;
  width: 24px;
  height: 24px;
  opacity: 0.4;
}
.leaf-ornament::before {
  content: '';
  display: block;
  width: 100%;
  height: 100%;
  border-radius: 0 50% 0 50%;
  background: linear-gradient(135deg, #b35a41, #dfcdb6);
}
.leaf-ornament--tl { top: 14px; left: 16px; }
.leaf-ornament--tr { top: 14px; right: 16px; transform: scaleX(-1); }
.leaf-ornament--bl { bottom: 14px; left: 16px; transform: scaleY(-1); }
.leaf-ornament--br { bottom: 14px; right: 16px; transform: scale(-1, -1); }

/* ── Responsive ── */
@media (max-width: 768px) {
  .cards-grid {
    grid-template-columns: 1fr;
    gap: 1.2em;
  }
  .verse-card {
    padding: 1.5em 1.5em;
    margin-bottom: 2em;
  }
  .form-transition-wrapper {
    margin-left: -10px;
    margin-right: -10px;
  }
}

/* ── Remove .well background from homepage ── */
.homepage-content > .well {
  background: transparent !important;
  border: none !important;
  box-shadow: none !important;
  padding: 0 !important;
}
</style>

<!-- ═══════ VERSE / QUOTE ═══════ -->
<div style="text-align: center; margin-top: 2em; margin-bottom: 0;">

<div class="card-base verse-card text-center" style="animation-delay: 0s; position: relative;">
  <div class="leaf-ornament leaf-ornament--tl"></div>
  <div class="leaf-ornament leaf-ornament--tr"></div>
  <p style="font-size: 1.3em; font-style: italic; color: #dfcdb6; margin: 0.5em 1em; line-height: 1.7; font-family: 'Playfair Display', 'Georgia', serif;">
    „Lépe je dvěma než jednomu, neboť mají lepší mzdu za svoji námahu.“
  </p>
  <p style="font-size: 0.95em; color: #e5a983; font-family: 'Lora', 'Georgia', serif; font-style: italic; margin-top: 1.2em; margin-bottom: 0; letter-spacing: 0.05em;">
    — Kazatel 4:9 —
  </p>
  <div class="leaf-ornament leaf-ornament--bl"></div>
  <div class="leaf-ornament leaf-ornament--br"></div>
</div>

</div>

<!-- ═══════ DIVIDER ═══════ -->
<div class="section-divider"></div>

<!-- ═══════ THREE CARD GRID ═══════ -->
<div class="cards-grid">

  <!-- Card 1: RSVP -->
  <div class="card-base rsvp-highlight" style="animation-delay: 0.1s;">
    <div>
      <h3 class="card-heading"><span class="card-icon card-icon--ring"></span> Potvrzení účasti</h3>
      <p class="card-text">Dejte nám prosím vědět ideálně do konce května, že dorazíte.</p>
    </div>
    <div style="margin-top: 2em;">
      <a href="#rsvp" class="custom-btn">Potvrdit účast</a>
    </div>
  </div>

  <!-- Card 2: When & Where -->
  <div class="card-base" style="animation-delay: 0.2s;">
    <div>
      <h3 class="card-heading"><span class="card-icon card-icon--cal"></span> Kdy a kde</h3>
      <p class="card-text"><strong style="color: #b6c8c2; font-size: 1.1em;">20. června 2026</strong></p>
      <p class="card-text"><strong style="color: #b6c8c2; font-size: 1.1em;">Rychtářův statek Raspenava</strong></p>
      <p class="card-text">Obřad začíná ve <strong style="color: #b6c8c2;">13:00</strong></p>
    </div>
    <div style="margin-top: 2em;">
      <a href="/page/venue/" class="custom-btn">Zobrazit místo</a>
    </div>
  </div>

  <!-- Card 3: Program -->
  <div class="card-base" style="animation-delay: 0.3s;">
    <div>
      <h3 class="card-heading"><span class="card-icon card-icon--timeline"></span> Program</h3>
      <p class="card-text">Od obřadu až po párty.</p>
      <p class="card-text">Podívejte se, co se chystá.</p>
    </div>
    <div style="margin-top: 2em;">
      <a href="/page/program/" class="custom-btn">Zobrazit program</a>
    </div>
  </div>

</div>

<!-- ═══════ DIVIDER ═══════ -->
<div class="section-divider"></div>

<!-- ═══════ RSVP FORM ═══════ -->
<div class="form-transition-wrapper" id="rsvp">
  <div style="max-width: 800px; margin: 0 auto; text-align: center;">
    <h2 style="margin-top: 0; color: #dfcdb6; font-family: 'Playfair Display', 'Georgia', serif; font-size: 2em; font-weight: 700;">Potvrzení účasti</h2>
    <p style="font-size: 1.1em; margin-bottom: 2em; color: #b6c8c2; font-family: 'Lora', 'Georgia', serif;">
      Dejte nám prosím vědět, zda dorazíte. Vyplňte formulář níže.
    </p>
  </div>

  <div class="form-card">
    <div style="text-align: center; overflow: hidden; border-radius: 12px; border: 1px solid rgba(223, 205, 182, 0.2); box-shadow: 0 10px 30px rgba(0,0,0,0.4);">
      <iframe src="https://docs.google.com/forms/d/e/1FAIpQLSdUHN6msQ5gtzGYLHRAadkjBgpQC2eSAnWYRumYUJy1tWdZCw/viewform?embeded=true" width="100%" height="550" frameborder="0" marginheight="0" marginwidth="0" style="background: #fff; filter: invert(90%) hue-rotate(180deg) brightness(1.05) contrast(1.05);"></iframe>
    </div>
  </div>
</div>

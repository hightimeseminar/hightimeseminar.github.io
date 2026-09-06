---
layout: page
title:
permalink: /program/
---
<div class="page-title programme-hero">

  <img
    src="{{ '/assets/img/htd-hero8.png' | relative_url }}"
    class="programme-hero-image"
    alt=""
    aria-hidden="true"
    loading="eager"
    fetchpriority="high"
  >

  <div class="programme-hero-overlay"></div>

  <div class="programme-hero-content">
    <h1 class="mono-bold">Programme</h1>
  </div>

</div>

<style>

  /* Remove empty Beautiful Jekyll header spacing */
  .header-section .intro-header {
    margin: 0 !important;
  }

  .page-title.programme-hero {
    position: relative !important;
    height: 300px !important;
    min-height: 0 !important;
    padding: 0 !important;
    box-sizing: border-box !important;
    overflow: hidden;

    display: flex;
    justify-content: center;
    align-items: center;

    /* dark fallback while image loads */
    background: #061923 !important;
  }

  .programme-hero-image {
    position: absolute;
    inset: 0;

    width: 100%;
    height: 100%;

    object-fit: cover;
    object-position: center 35%;

    z-index: 0;
  }

  .programme-hero-overlay {
    position: absolute;
    inset: 0;

    background: rgba(5, 30, 42, 0.30);

    z-index: 1;
  }

  .programme-hero-content {
    position: absolute;
    z-index: 2;

    left: 48%;
    top: 56%;
    transform: translate(-50%, -50%);

    text-align: center;
    white-space: nowrap;
  }

  .programme-hero-content h1 {
    color: white !important;
    margin: 0 !important;
  }

  @media (max-width: 768px) {

    .page-title.programme-hero {
      height: 250px !important;
    }

    .programme-hero-image {
      object-position: 68% center;
    }

    .programme-hero-content {
      left: 50%;
      top: 50%;
      width: 90%;
      white-space: normal;
    }
  }

</style>

<div style="margin-bottom: 30px; line-height: 1.7; font-size: 1.05em; color: #404040;">

  <p>
    Talks are held on <strong>Tuesdays at 12:00 UTC</strong> via Zoom.
    Each seminar consists of a <strong>50-minute presentation followed by Q&amp;A</strong>.
    The first three seminars will take place weekly, followed by a fortnightly schedule.
  </p>

  <hr>

  <h2>Upcoming talks</h2>

  <p>
    <strong>6 October 2026</strong><br>
    Speaker Name — University<br>
    <em>Title of talk</em>
  </p>

  <p>
    <strong>13 October 2026</strong><br>
    Speaker Name — University<br>
    <em>Title of talk</em>
  </p>

  <p>
    <strong>20 October 2026</strong><br>
    Speaker Name — University<br>
    <em>Title of talk</em>
  </p>

  <p>
    <strong>04 November 2026</strong><br>
    Speaker Name — University<br>
    <em>Title of talk</em>
   </p>

    <p>
    <strong>18 November 2026</strong><br>
    Speaker Name — University<br>
    <em>Title of talk</em>
  </p>

   <p>
    <strong>02 December 2026</strong><br>
    Speaker Name — University<br>
    <em>Title of talk</em>
  </p>

   <p>
    <strong>16 December 2026</strong><br>
    Speaker Name — University<br>
    <em>Title of talk</em>
  </p>

</div>

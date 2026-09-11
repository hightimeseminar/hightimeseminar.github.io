---
layout: page
title:
permalink: /program/
---

<!-- Page title banner -->
{% include hero.html title="Programme" image="/assets/img/htd-hero11.png" %}


<style>

/* =========================================================
   PROGRAMME PAGE
   ========================================================= */

<div class="programme-intro">
  <p>
    Talks are held on <strong>Tuesdays at 12:00 UTC</strong> via Zoom. Your local time is shown automatically for each seminar. Each seminar consists of a <strong>50-minute presentation followed by Q&amp;A</strong>.
    The first three seminars will take place weekly, followed by a fortnightly schedule.
  </p>

  <div class="time-converter">
    <div class="time-converter-text">
      <strong>Show talks in your local time</strong><br>
      <span>
        Your timezone is detected automatically, or you can choose another one.
      </span>
    </div>

    <select id="timezone-select" aria-label="Choose timezone"></select>
  </div>
</div>

/* =========================================================
   TALK CARDS
   ========================================================= */

.talk-card {
  background: #f7f7f7;
  border: 1px solid #dddddd;
  border-radius: 18px;

  padding: 24px 28px;

  margin-top: 25px;
  margin-bottom: 50px;

  box-shadow: 0 2px 6px rgba(0,0,0,0.04);
}


/* Date */
.talk-date {
  display: inline-block;

  background-color: #bb446c;
  color: white;

  font-family: monospace;
  font-size: 1.05em;
  font-weight: bold;
  letter-spacing: 0.04em;

  padding: 7px 13px;
  margin-bottom: 18px;

  border-radius: 6px;
}


/* Talk title */
.talk-title {
  margin: 4px 0 13px 0;

  font-size: 1.45em;
  line-height: 1.3;

  color: #292929;
}


/* Speaker */
.talk-speaker {
  font-size: 1.05em;
  color: #404040;

  margin-bottom: 18px;
}


/* Affiliation */
.talk-affiliation {
  margin-left: 7px;
  color: #666666;
}

.talk-affiliation::before {
  content: "— ";
}


/* Abstract */
.talk-abstract {
  border-top: 1px solid #dddddd;

  padding-top: 16px;

  line-height: 1.65;
  color: #444444;
}


/* Placeholder entries */
.talk-placeholder .talk-title {
  color: #666666;
  font-style: italic;
}

.talk-placeholder .talk-speaker {
  color: #777777;
}


/* =========================================================
   MOBILE
   ========================================================= */

@media (max-width: 768px) {

  .talk-card {
    padding: 20px;
    margin-bottom: 38px;
  }

  .talk-title {
    font-size: 1.3em;
  }

  .talk-affiliation {
    display: block;
    margin-left: 0;
    margin-top: 3px;
  }

  .talk-affiliation::before {
    content: "";
  }
}

   /* =========================================================
   TIMEZONE CONVERTER
   ========================================================= */

.time-converter {
  margin-top: 22px;
  padding: 16px 20px;

  border: 1px solid #dddddd;
  border-radius: 12px;

  background: #f7f7f7;

  display: flex;
  justify-content: space-between;
  align-items: center;
  gap: 20px;
}

.time-converter-text {
  line-height: 1.4;
}

.time-converter-text strong {
  color: #333333;
}

.time-converter-text span {
  color: #666666;
  font-size: 0.92em;
}

#timezone-select {
  min-width: 260px;

  padding: 9px 12px;

  border: 1px solid #cccccc;
  border-radius: 8px;

  background: white;
  color: #333333;

  font-size: 0.95em;
}


/* UTC + converted local time */

.talk-time {
  margin-top: -8px;
  margin-bottom: 18px;

  font-size: 0.95em;
}

.talk-utc {
  color: #666666;
  font-weight: bold;
}

.talk-local-time {
  margin-left: 10px;
  color: #276b77;
  font-weight: bold;
}

.talk-local-time::before {
  content: "→ ";
}


@media (max-width: 768px) {

  .time-converter {
    flex-direction: column;
    align-items: stretch;
  }

  #timezone-select {
    width: 100%;
    min-width: 0;
  }

  .talk-local-time {
    display: block;
    margin-left: 0;
    margin-top: 4px;
  }

  .talk-local-time::before {
    content: "Your time: ";
  }
}

</style>



<!-- =======================================================
     INTRODUCTION
     ======================================================= -->

<div class="programme-intro">

  <p>
    Talks are held on <strong>Tuesdays at 12:00 UTC</strong> via Zoom.
    Each seminar consists of a <strong>50-minute presentation followed by Q&amp;A</strong>.
    The first three seminars will take place weekly, followed by a fortnightly schedule.
  </p>

</div>


<hr>


<h2>Upcoming talks</h2>



<!-- =======================================================
     6 OCTOBER
     ======================================================= -->

<div class="talk-card">

  <div class="talk-date">
    6 October 2026
  </div>

  <div class="talk-time">
  <span class="talk-utc">12:00 UTC</span>
  <span
    class="talk-local-time"
    data-utc="2026-10-06T12:00:00Z">
  </span>
</div>

  <h3 class="talk-title">
    Higher Time Derivatives: the Good, the Bad and the Ugly
  </h3>

  <div class="talk-speaker">
    <strong>Richard Woodard</strong>
    <span class="talk-affiliation">University of Florida</span>
  </div>

  <div class="talk-abstract">
    <strong>Abstract.</strong>
    Aside from philosophical interest, Lagrangians that contain higher time
    derivatives hold great interest for quantum gravity owing to the theorem
    of the late Kelly Stelle that adding fundamental Ricci-squared and
    Weyl-squared terms to the Hilbert action would result in a perturbatively
    renormalizable theory. The reason we still have a ``problem of quantum
    gravity'' is that the Weyl-squared term is not allowed. I explain why not,
    and hopefully debunk some of the confused and confusing literature on
    this subject. This talk is based on astro-ph/0601672, arXiv:1506.022,
    arXiv:2306.09596 and arXiv:2602.16190.
  </div>

</div>



<!-- =======================================================
     13 OCTOBER
     ======================================================= -->

<div class="talk-card talk-placeholder">

  <div class="talk-date">
    13 October 2026
  </div>

  <div class="talk-time">
  <span class="talk-utc">12:00 UTC</span>
  <span
    class="talk-local-time"
    data-utc="2026-10-13T12:00:00Z">
  </span>
</div>

  <h3 class="talk-title">
    Title to be announced
  </h3>

  <div class="talk-speaker">
    <strong>Alexander Vikman</strong>
    <span class="talk-affiliation">FZU - Institute of Physics of the Czech Academy of Sciences</span>
  </div>

</div>



<!-- =======================================================
     20 OCTOBER
     ======================================================= -->

<div class="talk-card talk-placeholder">

  <div class="talk-date">
    20 October 2026
  </div>

  <div class="talk-time">
  <span class="talk-utc">12:00 UTC</span>
  <span
    class="talk-local-time"
    data-utc="2026-10-20T12:00:00Z">
  </span>
</div>

  <h3 class="talk-title">
    Title to be announced
  </h3>

  <div class="talk-speaker">
    <strong>Speaker to be announced</strong>
    <span class="talk-affiliation">Affiliation</span>
  </div>

</div>



<!-- =======================================================
     3 NOVEMBER
     ======================================================= -->

<div class="talk-card talk-placeholder">

  <div class="talk-date">
    3 November 2026
  </div>

  <div class="talk-time">
  <span class="talk-utc">12:00 UTC</span>
  <span
    class="talk-local-time"
    data-utc="2026-11-03T12:00:00Z">
  </span>
</div>

  <h3 class="talk-title">
    Title to be announced
  </h3>

  <div class="talk-speaker">
    <strong>Shinji Mukohyama</strong>
    <span class="talk-affiliation">Yukawa Institute for Theoretical Physics (YITP), Kyoto University</span>
  </div>

</div>



<!-- =======================================================
     17 NOVEMBER
     ======================================================= -->

<div class="talk-card talk-placeholder">

  <div class="talk-date">
    17 November 2026
  </div>

  <div class="talk-time">
  <span class="talk-utc">12:00 UTC</span>
  <span
    class="talk-local-time"
    data-utc="2026-11-17T12:00:00Z">
  </span>
</div>

  <h3 class="talk-title">
    Title to be announced
  </h3>

  <div class="talk-speaker">
    <strong>Aaron Held</strong>
    <span class="talk-affiliation">École Normale Supérieure (ENS) Paris</span>
  </div>

</div>



<!-- =======================================================
     1 DECEMBER
     ======================================================= -->

<div class="talk-card talk-placeholder">

  <div class="talk-date">
    1 December 2026
  </div>

  <div class="talk-time">
  <span class="talk-utc">12:00 UTC</span>
  <span
    class="talk-local-time"
    data-utc="2026-12-01T12:00:00Z">
  </span>
</div>

  <h3 class="talk-title">
    Title to be announced
  </h3>

  <div class="talk-speaker">
    <strong>Speaker to be announced</strong>
    <span class="talk-affiliation">Affiliation</span>
  </div>

</div>



<!-- =======================================================
     15 DECEMBER
     ======================================================= -->

<div class="talk-card talk-placeholder">

  <div class="talk-date">
    15 December 2026
  </div>

  <div class="talk-time">
  <span class="talk-utc">12:00 UTC</span>
  <span
    class="talk-local-time"
    data-utc="2026-12-15T12:00:00Z">
  </span>
</div>

  <h3 class="talk-title">
    Title to be announced
  </h3>

  <div class="talk-speaker">
    <strong>Speaker to be announced</strong>
    <span class="talk-affiliation">Affiliation</span>
  </div>

</div>

<script>
(function () {

  const select = document.getElementById("timezone-select");
  const localTimes = document.querySelectorAll(".talk-local-time");

  if (!localTimes.length) return;

  /* Detect visitor's timezone */
  const detectedZone =
    Intl.DateTimeFormat().resolvedOptions().timeZone || "UTC";


  /* Convert all talk times */
  function updateTimes(zone) {

    localTimes.forEach(function(element) {

      const utcString = element.getAttribute("data-utc");
      const utcDate = new Date(utcString);

      if (isNaN(utcDate.getTime())) {
        element.textContent = "Invalid date";
        return;
      }

      try {

        const formatter = new Intl.DateTimeFormat(
          "en-GB",
          {
            timeZone: zone,
            weekday: "short",
            day: "numeric",
            month: "short",
            year: "numeric",
            hour: "2-digit",
            minute: "2-digit",
            hour12: false,
            timeZoneName: "short"
          }
        );

        element.textContent = formatter.format(utcDate);

      } catch (error) {

        element.textContent = utcDate.toLocaleString("en-GB");

      }

    });
  }


  /* Immediately show visitor's local time */
  updateTimes(detectedZone);


  /* If the timezone selector exists, populate it */
  if (select) {

    let zones = [];

    if (
      typeof Intl.supportedValuesOf === "function"
    ) {
      zones = Intl.supportedValuesOf("timeZone");
    } else {
      zones = [
        "Europe/London",
        "Europe/Paris",
        "Europe/Berlin",
        "Europe/Madrid",
        "America/New_York",
        "America/Chicago",
        "America/Denver",
        "America/Los_Angeles",
        "America/Sao_Paulo",
        "Asia/Jerusalem",
        "Asia/Kolkata",
        "Asia/Taipei",
        "Asia/Tokyo",
        "Australia/Sydney"
      ];
    }

    /* Add UTC explicitly */
    if (!zones.includes("UTC")) {
      zones.unshift("UTC");
    }

    /* Add detected timezone if necessary */
    if (!zones.includes(detectedZone)) {
      zones.unshift(detectedZone);
    }

    zones.forEach(function(zone) {

      const option = document.createElement("option");

      option.value = zone;
      option.textContent = zone.replace(/_/g, " ");

      if (zone === detectedZone) {
        option.selected = true;
      }

      select.appendChild(option);

    });


    select.addEventListener("change", function() {
      updateTimes(select.value);
    });

  }

})();
</script>




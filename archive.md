---
layout: page
title: 
permalink: /archive/
---
<div class="page-title archive-hero">

  <img
    src="{{ '/assets/img/htd-hero5.png' | relative_url }}"
    class="archive-hero-image"
    alt=""
    aria-hidden="true"
  >

  <div class="archive-hero-overlay"></div>

  <div class="archive-hero-content">
    <h1 class="mono-bold">Presentation Archive</h1>
  </div>

</div>

<style>

  .page-title.archive-hero {
    position: relative !important;
    height: 300px !important;
    min-height: 0 !important;
    padding: 0 !important;
    overflow: hidden;

    display: flex;
    justify-content: center;
    align-items: center;
  }

  .archive-hero-image {
    position: absolute;
    inset: 0;

    width: 100%;
    height: 100%;

    object-fit: cover;
    object-position: center top;

    z-index: 0;
  }

  .archive-hero-overlay {
    position: absolute;
    inset: 0;

    background: rgba(5, 30, 42, 0.32);

    z-index: 1;
  }

  .archive-hero-content {
    position: absolute;
    z-index: 2;

    left: 48%;
    top: 50%;
    transform: translate(-50%, -50%);

    text-align: center;
    white-space: nowrap;
  }

  .archive-hero-content h1 {
    color: white !important;
    margin: 0 !important;
  }

  @media (max-width: 768px) {

    .page-title.archive-hero {
      height: 250px !important;
    }

    .archive-hero-image {
      object-position: 65% center;
    }

    .archive-hero-content {
      left: 50%;
      white-space: normal;
      width: 90%;
    }
  }

</style>


<!-- 1. SEARCH AND SORT CONTROL BAR -->
<div style="display: flex; justify-content: space-between; align-items: center; margin-bottom: 25px; gap: 15px; flex-wrap: wrap;">
  
  <!-- Search Input Box -->
  <input 
    id="archive-search" 
    type="text" 
    placeholder="🔍 Search by title, speaker, or keywords..." 
    style="flex-grow: 1; max-width: 400px; padding: 8px 16px; border: 1px solid #ddd; border-radius: 25px; outline: none; font-size: 0.9em; transition: border-color 0.2s; background-color: #fff; color: #333;"
    onfocus="this.style.borderColor='#0085A1'"
    onblur="this.style.borderColor='#ddd'"
  >
  
  <!-- Sort Toggle Button -->
  <button 
    id="sort-toggle" 
    style="background-color: #fff; color: #575757; border: 1px solid #ddd; padding: 8px 16px; border-radius: 20px; cursor: pointer; font-size: 0.9em; transition: all 0.2s ease; white-space: nowrap; outline: none;"
    onmouseover="this.style.borderColor='#0085A1'; this.style.color='#0085A1';"
    onmouseout="this.style.borderColor='#ddd'; this.style.color='#575757';"
  >
    Order: Newest First
  </button>
  
</div>

<hr>

<!-- 2. THE TALK CONTAINER BOX -->
<div id="talks-container">
  {% assign sorted_talks = site.data.past_talks | sort: "no" | reversed %}
  {% for talk in sorted_talks %}
  <div class="talk-window" style="margin-bottom: 20px;">
    <details style="border: 1px solid #ddd; padding: 20px; border-radius: 25px; background-color: #eeeeee85; box-shadow: 0 2px 4px rgba(0,0,0,0.02);">
      
      <summary style="cursor: pointer; list-style: none; outline: none;">
        <div style="display: flex; justify-content: space-between; align-items: center; flex-wrap: wrap;">
          <div>
            <h3 style="margin: 0 0 5px 0; color: #555;"> {{ talk.title }}</h3>
            <strong style="color: #555;">Speaker:</strong> {{ talk.speaker }} &nbsp;|&nbsp; <strong style="color: #555;">Date:</strong> {{ talk.date }}
          </div>
          <span style="color: #555; font-size: 0.9em; background-color: #fff; border: 1px solid #ddd; padding: 6px 14px; border-radius: 20px; margin-top: 10px; display: inline-block; transition: all 0.2s; font-weight: 500;">
            ➕ Show Details & Video
          </span>
        </div>
      </summary>

      <hr style="margin: 20px 0;">

      <!-- REORDERED INNER CONTENT VAULT -->
      <div style="padding: 0 20px;">
        
        <h4>Abstract</h4>
        <p style="margin-bottom: 20px;">{{ talk.abstract }}</p>

        <h4>About the Speaker</h4>
        <p style="margin-bottom: 20px;">{{ talk.about }}</p>

        <h4>Recording</h4>
        <div style="position: relative; padding-bottom: 56.25%; height: 0; overflow: hidden; max-width: 100%; margin-bottom: 20px; border-radius: 4px;">
          <iframe 
            src="https://www.youtube.com/embed/{{ talk.youtube_id }}" 
            srcdoc="<style>*{padding:0;margin:0;overflow:hidden}html,body{height:100%}img,span{position:absolute;width:100%;top:0;bottom:0;margin:auto}span{height:1.5em;text-align:center;font:48px/1.5 sans-serif;color:white;text-shadow:0 0 0.5em rgba(0,0,0,0.5)}</style><a href=https://www.youtube.com/embed/{{ talk.youtube_id }}?autoplay=1><img src=https://img.youtube.com/vi/{{ talk.youtube_id }}/hqdefault.jpg alt='Play Video'><span>▶</span></a>"
            style="position: absolute; top: 0; left: 0; width: 100%; height: 100%; border:0;" 
            allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" 
            allowfullscreen
            loading="lazy">
          </iframe>
        </div>

      </div>

    </details>
  </div>
  {% endfor %}
</div>


<!-- COMBINED CONTROLS SCRIPT -->
<script>
  const toggleBtn = document.getElementById('sort-toggle');
  const searchInput = document.getElementById('archive-search');
  const container = document.getElementById('talks-container');
  let newestFirst = true;

  // SORT ENGINE
  toggleBtn.addEventListener('click', () => {
    const elements = Array.from(container.getElementsByClassName('talk-window'));
    elements.reverse();
    elements.forEach(el => container.appendChild(el));
    newestFirst = !newestFirst;
    toggleBtn.innerText = newestFirst ? "🔄 Order: Newest First" : "🔄 Order: Oldest First";
  });

  // SEARCH ENGINE
  searchInput.addEventListener('input', (e) => {
    const query = e.target.value.toLowerCase().trim();
    const elements = Array.from(container.getElementsByClassName('talk-window'));

    elements.forEach(el => {
      const cardText = el.innerText.toLowerCase();
      if (cardText.includes(query)) {
        el.style.display = 'block';
      } else {
        el.style.display = 'none';
      }
    });
  });
</script>

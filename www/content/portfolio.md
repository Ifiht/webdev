---
title: "Portfolio"
date: 2023-12-18T15:12:40-05:00
draft: false
description = "To-Do: describe me!"
---

<style>
    .iframe-container {
        display: flex;
        flex-wrap: wrap;
        align-items: center; 
        justify-content: space-around;
    }

    .iframe-wrapper {
      position: relative;
      flex: 1;
      width: 100%; /* Full width initially */
      max-width: 400px; /* Maximum width for small screens */
      max-height: 400px; /* Maximum width for small screens */
      margin-right: 10px; /* Adjust the margin between iframes as needed */
      padding-bottom: 50%; /* 1:1 aspect ratio for the iframe */
    }

    iframe {
      position: absolute;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
    }

    .overlay {
      position: absolute;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      background: rgba(0, 0, 0, 0); /* Initially transparent background */
      cursor: pointer;
      transition: background 0.3s ease; /* Smooth transition effect for background */
    }

    .overlay:hover {
      background: rgba(0, 0, 0, 0.7); /* Semi-transparent black overlay on hover */
    }

    .overlay-text {
        position: absolute;
        top: 50%;
        left: 50%;
        transform: translate(-50%, -50%);
        color: white;
        font-size: 36px;
        font-weight: bold;
        opacity: 0; /* Initially transparent text */
        transition: opacity 0.3s ease; /* Smooth transition effect for text */
    }

    .overlay:hover .overlay-text {
      opacity: 1; /* Make text fully visible on hover */
    }
    
    /* Media query for larger screens */
    @media (min-width: 600px) {
      .iframe-wrapper {
        width: 50%; /* Adjust the width for larger screens */
      }
    }
</style>

<div class="iframe-container">
    <div class="iframe-wrapper">
    <iframe src="https://www.pacificpokertour.com/" frameborder="0" allowfullscreen></iframe>
    <div class="overlay" onclick="handleOverlayClick('https://www.pacificpokertour.com/')">
        <div class="overlay-text">Visit</div>
    </div>
    </div>
    <div class="iframe-wrapper">
    <iframe src="https://webdev.evlis.org/oldsite/index.html" frameborder="0" allowfullscreen></iframe>
    <div class="overlay" onclick="handleOverlayClick('https://webdev.evlis.org/oldsite/index.html')">
        <div class="overlay-text">Visit</div>
    </div>
    </div>
</div>


<script>
  function handleOverlayClick(url) {
    // Handle click event for the overlay
    //alert("Overlay clicked!");
    window.open(url);
  }
</script>

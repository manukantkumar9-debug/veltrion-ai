<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">

  <meta name="theme-color" content="#050806">
  <meta name="description" content="Veltrion AI — Premium AI Image Ads and Video Ads for brands and businesses.">

  <title>Veltrion AI | AI Advertising Studio</title>

  <style>
    :root {
      --bg: #050806;
      --card: #0D1511;
      --section: #101A14;
      --green: #36E89A;
      --bright: #75FFB8;
      --white: #F5F7F5;
      --muted: #A7B3AA;
      --border: #24352B;
    }

    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    html {
      scroll-behavior: smooth;
      scroll-padding-top: 90px;
    }

    body {
      background: var(--bg);
      color: var(--white);
      font-family: Arial, Helvetica, sans-serif;
      line-height: 1.6;
      overflow-x: hidden;
    }

    a {
      color: inherit;
      text-decoration: none;
    }

    button {
      font: inherit;
      cursor: pointer;
    }

    button:focus-visible,
    a:focus-visible {
      outline: 2px solid var(--bright);
      outline-offset: 4px;
    }

    .container {
      width: min(1180px, 92%);
      margin: auto;
    }

    .green {
      color: var(--green);
    }

    .eyebrow {
      color: var(--green);
      font-size: 12px;
      font-weight: 800;
      letter-spacing: 2px;
      text-transform: uppercase;
    }

    .section {
      padding: 76px 0;
    }

    .section-heading {
      display: flex;
      justify-content: space-between;
      align-items: end;
      gap: 20px;
      margin-bottom: 28px;
    }

    .section-heading h2 {
      font-size: clamp(27px, 4vw, 42px);
      line-height: 1.2;
      margin-top: 8px;
    }

    .section-heading p {
      color: var(--muted);
      font-size: 14px;
      max-width: 430px;
      margin-top: 10px;
    }

    /* NAVBAR */

    .navbar {
      position: sticky;
      top: 0;
      z-index: 100;
      background: rgba(5, 8, 6, 0.95);
      border-bottom: 1px solid var(--border);
      backdrop-filter: blur(14px);
    }

    .nav-inner {
      min-height: 76px;
      display: flex;
      align-items: center;
      justify-content: space-between;
      gap: 20px;
    }

    .brand {
      font-size: 22px;
      font-weight: 900;
      letter-spacing: -0.7px;
      white-space: nowrap;
    }

    .brand span {
      color: var(--green);
    }

    .nav-links {
      display: flex;
      align-items: center;
      gap: 22px;
    }

    .nav-links a {
      color: var(--muted);
      font-size: 13px;
      transition: color 0.2s;
    }

    .nav-links a:hover {
      color: var(--green);
    }

    .btn {
      display: inline-flex;
      align-items: center;
      justify-content: center;
      gap: 8px;
      min-height: 44px;
      padding: 11px 18px;
      border: 1px solid var(--green);
      border-radius: 7px;
      background: var(--green);
      color: #041109;
      font-size: 13px;
      font-weight: 800;
      transition: 0.2s;
    }

    .btn:hover {
      background: var(--bright);
      transform: translateY(-2px);
    }

    .btn-outline {
      color: var(--green);
      background: transparent;
    }

    .btn-outline:hover {
      color: #041109;
      background: var(--green);
    }

    .menu-toggle {
      display: none;
      color: var(--green);
      background: transparent;
      border: 1px solid var(--border);
      border-radius: 6px;
      padding: 7px 11px;
      font-size: 21px;
    }

    /* HERO */

    .hero {
      padding: 76px 0 84px;
      background:
        radial-gradient(
          ellipse at 80% 30%,
          rgba(54, 232, 154, 0.09),
          transparent 43%
        );
    }

    .hero-grid {
      display: grid;
      grid-template-columns: 1.05fr 0.95fr;
      align-items: center;
      gap: 46px;
    }

    .hero h1 {
      font-size: clamp(38px, 5.5vw, 65px);
      line-height: 1.08;
      letter-spacing: -2px;
      margin: 20px 0;
    }

    .hero-description {
      max-width: 510px;
      color: var(--muted);
      font-size: 16px;
      margin-bottom: 27px;
    }

    .hero-buttons {
      display: flex;
      flex-wrap: wrap;
      gap: 12px;
    }

    .hero-note {
      color: var(--muted);
      font-size: 12px;
      margin-top: 22px;
    }

    /* EMPTY PLACEHOLDER
       Later, your own uploaded artwork can go here. */

    .hero-placeholder {
      min-height: 350px;
      border: 1px dashed #355541;
      border-radius: 18px;
      background:
        radial-gradient(
          circle at center,
          rgba(54, 232, 154, 0.07),
          transparent 65%
        ),
        var(--card);
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      text-align: center;
      padding: 24px;
    }

    .placeholder-symbol {
      width: 68px;
      height: 68px;
      border: 1px solid var(--green);
      border-radius: 18px;
      display: grid;
      place-items: center;
      color: var(--green);
      font-size: 28px;
      margin-bottom: 20px;
    }

    .hero-placeholder h3 {
      font-size: 19px;
      margin-bottom: 8px;
    }

    .hero-placeholder p {
      max-width: 260px;
      color: var(--muted);
      font-size: 12px;
    }

    /* FEATURE STRIP */

    .feature-strip {
      border-top: 1px solid var(--border);
      border-bottom: 1px solid var(--border);
      background: #080D09;
    }

    .feature-grid {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
    }

    .feature {
      padding: 23px 15px;
      text-align: center;
      border-right: 1px solid var(--border);
    }

    .feature:last-child {
      border-right: none;
    }

    .feature strong {
      display: block;
      font-size: 14px;
      color: var(--white);
    }

    .feature span {
      display: block;
      color: var(--muted);
      font-size: 12px;
      margin-top: 3px;
    }

    /* CATEGORY FILTERS */

    .category-filters {
      display: flex;
      gap: 9px;
      flex-wrap: wrap;
      margin-bottom: 26px;
    }

    .filter-btn {
      border: 1px solid var(--border);
      border-radius: 6px;
      background: var(--card);
      color: var(--muted);
      padding: 9px 13px;
      font-size: 12px;
      transition: 0.2s;
    }

    .filter-btn:hover,
    .filter-btn.active {
      border-color: var(--green);
      background: rgba(54, 232, 154, 0.1);
      color: var(--green);
    }

    /* HORIZONTAL GALLERY */

    .gallery-controls {
      display: flex;
      gap: 8px;
      flex-shrink: 0;
    }

    .arrow-btn {
      width: 40px;
      height: 40px;
      border: 1px solid var(--border);
      border-radius: 7px;
      background: var(--card);
      color: var(--green);
      font-size: 19px;
    }

    .arrow-btn:hover {
      border-color: var(--green);
      background: var(--section);
    }

    .gallery {
      display: grid;
      grid-auto-flow: column;
      grid-auto-columns: calc((100% - 36px) / 3);
      gap: 18px;
      overflow-x: auto;
      overscroll-behavior-inline: contain;
      scroll-snap-type: x mandatory;
      scroll-behavior: smooth;
      scrollbar-width: thin;
      scrollbar-color: var(--green) var(--card);
      padding-bottom: 14px;
    }

    .gallery::-webkit-scrollbar {
      height: 5px;
    }

    .gallery::-webkit-scrollbar-track {
      background: var(--card);
    }

    .gallery::-webkit-scrollbar-thumb {
      background: var(--green);
      border-radius: 10px;
    }

    .ad-card {
      min-width: 0;
      overflow: hidden;
      border: 1px solid var(--border);
      border-radius: 11px;
      background: var(--card);
      scroll-snap-align: start;
      transition: border-color 0.2s, transform 0.2s;
    }

    .ad-card:hover {
      border-color: var(--green);
      transform: translateY(-3px);
    }

    /* EMPTY AD AREA: NO IMAGE FILES */

    .ad-placeholder {
      aspect-ratio: 4 / 5;
      min-height: 120px;
      display: flex;
      align-items: center;
      justify-content: center;
      text-align: center;
      padding: 10px;
      background:
        linear-gradient(
          145deg,
          rgba(54, 232, 154, 0.045),
          transparent 65%
        ),
        #080D09;
      border-bottom: 1px dashed #355541;
    }

    .ad-placeholder-inner {
      color: #81968A;
      font-size: 12px;
    }

    .ad-placeholder-inner span {
      display: block;
      color: var(--green);
      font-size: 23px;
      margin-bottom: 8px;
    }

    .ad-info {
      padding: 13px;
    }

    .ad-category {
      color: var(--green);
      font-size: 10px;
      font-weight: 800;
      letter-spacing: 1px;
      text-transform: uppercase;
    }

    .ad-info h3 {
      font-size: 14px;
      margin: 5px 0 12px;
    }

    .card-btn {
      width: 100%;
      min-height: 38px;
      padding: 8px;
      font-size: 11px;
    }

    .gallery-note {
      color: var(--muted);
      font-size: 12px;
      margin-top: 13px;
    }

    /* VIDEO PLACEHOLDERS */

    .video-placeholder {
      aspect-ratio: 4 / 5;
      min-height: 120px;
      display: flex;
      align-items: center;
      justify-content: center;
      border-bottom: 1px dashed #355541;
      background:
        radial-gradient(
          circle,
          rgba(54, 232, 154, 0.08),
          transparent 65%
        ),
        #080D09;
    }

    .play-button {
      width: 48px;
      height: 48px;
      border: 1px solid var(--green);
      border-radius: 50%;
      color: var(--green);
      background: rgba(54, 232, 154, 0.06);
      font-size: 18px;
      display: grid;
      place-items: center;
    }

    /* BUSINESS SECTION */

    .business-panel {
      padding: 48px;
      border: 1px solid var(--border);
      border-radius: 15px;
      background:
        radial-gradient(
          ellipse at right,
          rgba(54, 232, 154, 0.1),
          transparent 55%
        ),
        var(--section);
      display: flex;
      align-items: center;
      justify-content: space-between;
      gap: 30px;
    }

    .business-panel h2 {
      font-size: clamp(26px, 4vw, 40px);
      line-height: 1.2;
      margin: 12px 0;
    }

    .business-panel p {
      max-width: 570px;
      color: var(--muted);
      font-size: 14px;
    }

    /* ABOUT */

    .about-grid {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      gap: 16px;
    }

    .about-card {
      padding: 23px;
      border: 1px solid var(--border);
      border-radius: 10px;
      background: var(--card);
    }

    .about-card h3 {
      font-size: 16px;
      margin-bottom: 9px;
    }

    .about-card p {
      color: var(--muted);
      font-size: 13px;
    }

    /* CONTACT */

    .contact-panel {
      text-align: center;
      padding: 46px 20px;
      border: 1px solid var(--border);
      border-radius: 14px;
      background: var(--card);
    }

    .contact-panel h2 {
      font-size: clamp(28px, 4vw, 42px);
      margin: 12px 0;
    }

    .contact-panel p {
      max-width: 550px;
      margin: 0 auto 23px;
      color: var(--muted);
      font-size: 14px;
    }

    .contact-status {
      color: var(--muted);
      font-size: 12px;
      margin-top: 14px;
    }

    /* FOOTER */

    footer {
      padding: 28px 0;
      border-top: 1px solid var(--border);
      background: #030504;
    }

    .footer-inner {
      display: flex;
      justify-content: space-between;
      align-items: center;
      gap: 18px;
    }

    .footer-inner p {
      color: var(--muted);
      font-size: 12px;
    }

    .footer-links {
      display: flex;
      gap: 18px;
      flex-wrap: wrap;
    }

    .footer-links a {
      color: var(--muted);
      font-size: 12px;
    }

    .footer-links a:hover {
      color: var(--green);
    }

    .hidden {
      display: none !important;
    }

    /* TABLET */

    @media (max-width: 850px) {
      .nav-links {
        gap: 12px;
      }

      .nav-links a {
        font-size: 12px;
      }

      .nav-contact {
        display: none;
      }

      .hero-grid {
        gap: 25px;
      }

      .hero h1 {
        font-size: 43px;
      }

      .hero-placeholder {
        min-height: 290px;
      }

      .gallery {
        grid-auto-columns: calc((100% - 18px) / 2);
      }

      .business-panel {
        padding: 32px;
      }
    }

    /* MOBILE */

    @media (max-width: 600px) {
      .container {
        width: 94%;
      }

      .nav-inner {
        min-height: 65px;
      }

      .brand {
        font-size: 19px;
      }

      .menu-toggle {
        display: block;
      }

      .nav-links {
        display: none;
        position: absolute;
        top: 65px;
        left: 0;
        right: 0;
        padding: 18px 5%;
        background: #080D09;
        border-bottom: 1px solid var(--border);
        flex-direction: column;
        align-items: stretch;
        gap: 0;
      }

      .nav-links.open {
        display: flex;
      }

      .nav-links a {
        padding: 12px 0;
        font-size: 14px;
      }

      .hero {
        padding: 48px 0;
      }

      .hero-grid {
        grid-template-columns: 1fr;
        gap: 28px;
      }

      .hero h1 {
        font-size: clamp(37px, 10vw, 48px);
      }

      .hero-description {
        font-size: 14px;
      }

      .hero-placeholder {
        min-height: 220px;
      }

      .section {
        padding: 53px 0;
      }

      .section-heading {
        align-items: center;
        gap: 10px;
      }

      .section-heading h2 {
        font-size: 25px;
      }

      .section-heading p {
        font-size: 12px;
      }

      .gallery-controls {
        gap: 5px;
      }

      .arrow-btn {
        width: 33px;
        height: 36px;
        font-size: 16px;
      }

      /* THREE CARDS VISIBLE ON MOBILE */

      .gallery {
        grid-auto-columns: calc((100% - 16px) / 3);
        gap: 8px;
      }

      .ad-placeholder,
      .video-placeholder {
        min-height: 95px;
        aspect-ratio: 3 / 4;
        padding: 4px;
      }

      .ad-placeholder-inner {
        font-size: 9px;
      }

      .ad-placeholder-inner span {
        font-size: 17px;
        margin-bottom: 4px;
      }

      .ad-info {
        padding: 7px;
      }

      .ad-category {
        font-size: 8px;
        letter-spacing: 0;
      }

      .ad-info h3 {
        font-size: 10px;
        line-height: 1.35;
        min-height: 27px;
      }

      .card-btn {
        font-size: 9px;
        padding: 6px 3px;
        min-height: 34px;
      }

      .play-button {
        width: 30px;
        height: 30px;
        font-size: 12px;
      }

      .filter-btn {
        padding: 7px 9px;
        font-size: 10px;
      }

      .feature {
        padding: 15px 5px;
      }

      .feature strong {
        font-size: 11px;
      }

      .feature span {
        font-size: 9px;
      }

      .business-panel {
        padding: 25px 18px;
        flex-direction: column;
        align-items: flex-start;
      }

      .about-grid {
        grid-template-columns: 1fr;
      }

      .about-card {
        padding: 18px;
      }

      .footer-inner {
        flex-direction: column;
        align-items: flex-start;
      }
    }

    @media (prefers-reduced-motion: reduce) {
      html {
        scroll-behavior: auto;
      }

      *,
      *::before,
      *::after {
        transition-duration: 0.01ms !important;
        animation-duration: 0.01ms !important;
      }
    }
  </style>
</head>

<body>

  <!-- NAVBAR -->

  <header class="navbar">
    <div class="container nav-inner">

      <a class="brand" href="#home" aria-label="Veltrion AI Home">
        VELTRION<span> AI</span>
      </a>

      <button
        class="menu-toggle"
        id="menuToggle"
        aria-label="Open navigation menu"
        aria-expanded="false"
        aria-controls="navLinks"
      >☰</button>

      <nav class="nav-links" id="navLinks">
        <a href="#home">Home</a>
        <a href="#image-ads">Image Ads</a>
        <a href="#video-ads">Video Ads</a>
        <a href="#about">About</a>
        <a href="#contact">Contact</a>
      </nav>

      <a class="btn nav-contact" href="#contact">Contact Us ↗</a>

    </div>
  </header>


  <main>

    <!-- HERO SECTION -->

    <section class="hero" id="home">
      <div class="container hero-grid">

        <div>
          <span class="eyebrow">AI Advertising Studio</span>

          <h1>
            Your Products.<br>
            Our Creativity.<br>
            <span class="green">Powered by AI.</span>
          </h1>

          <p class="hero-description">
            We create premium AI-powered image and video advertisements
            that help brands present their products with creativity,
            style and impact.
          </p>

          <div class="hero-buttons">
            <a class="btn" href="#image-ads">Explore Image Ads ↗</a>
            <a class="btn btn-outline" href="#video-ads">Explore Video Ads</a>
          </div>

          <p class="hero-note">
            Creative advertising for products, brands and businesses.
          </p>
        </div>

        <!-- EMPTY: ADD YOUR OWN VISUAL LATER -->

        <div class="hero-placeholder">
          <div class="placeholder-symbol">+</div>
          <h3>Your Creative Goes Here</h3>
          <p>
            Empty space reserved for your own uploaded artwork
            or future 3D robot.
          </p>
        </div>

      </div>
    </section>


    <!-- FEATURES -->

    <section class="feature-strip">
      <div class="container feature-grid">

        <div class="feature">
          <strong>AI Image Ads</strong>
          <span>Product advertising creatives</span>
        </div>

        <div class="feature">
          <strong>AI Video Ads</strong>
          <span>Creative video advertising</span>
        </div>

        <div class="feature">
          <strong>Brand Projects</strong>
          <span>Custom creative solutions</span>
        </div>

      </div>
    </section>


    <!-- IMAGE ADS -->

    <section class="section" id="image-ads">
      <div class="container">

        <div class="section-heading">
          <div>
            <span class="eyebrow">Our Creative Portfolio</span>
            <h2>Explore <span class="green">Image Ads</span></h2>
            <p>
              Explore product advertising concepts across
              different industries and categories.
            </p>
          </div>

          <div class="gallery-controls">
            <button
              class="arrow-btn"
              data-target="imageGallery"
              data-direction="-1"
              aria-label="Previous image ads"
            >←</button>

            <button
              class="arrow-btn"
              data-target="imageGallery"
              data-direction="1"
              aria-label="Next image ads"
            >→</button>
          </div>
        </div>


        <!-- CATEGORY FILTERS -->

        <div class="category-filters" id="categoryFilters">
          <button class="filter-btn active" data-category="all">All</button>
          <button class="filter-btn" data-category="electronics">Electronics</button>
          <button class="filter-btn" data-category="fashion">Fashion</button>
          <button class="filter-btn" data-category="beauty">Beauty</button>
          <button class="filter-btn" data-category="food">Food</button>
          <button class="filter-btn" data-category="home">Home & Kitchen</button>
          <button class="filter-btn" data-category="jewelry">Jewelry</button>
          <button class="filter-btn" data-category="automotive">Automotive</button>
          <button class="filter-btn" data-category="sports">Sports</button>
          <button class="filter-btn" data-category="furniture">Furniture</button>
          <button class="filter-btn" data-category="gaming">Computers & Gaming</button>
        </div>

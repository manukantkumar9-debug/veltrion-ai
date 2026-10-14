<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">

  <meta name="theme-color" content="#050806">
  <meta name="description"
        content="Veltrion AI creates premium AI-powered image ads and video ads for modern brands.">

  <title>Veltrion AI — Creative Intelligence</title>

  <style>
    /* =========================================
       VELTRION AI — DESIGN SYSTEM
    ========================================= */

    :root {
      --bg: #050806;
      --card: #0D1511;
      --section: #101A14;
      --green: #36E89A;
      --bright: #75FFB8;
      --text: #F5F7F5;
      --muted: #A7B3AA;
      --border: #24352B;

      --radius: 22px;
      --container: 1180px;
    }

    *,
    *::before,
    *::after {
      box-sizing: border-box;
    }

    html {
      scroll-behavior: smooth;
      scroll-padding-top: 90px;
    }

    body {
      margin: 0;
      background: var(--bg);
      color: var(--text);
      font-family: Inter, -apple-system, BlinkMacSystemFont,
                   "Segoe UI", sans-serif;
      line-height: 1.6;
      overflow-x: hidden;
    }

    body,
    button,
    a {
      -webkit-tap-highlight-color: transparent;
    }

    a {
      color: inherit;
      text-decoration: none;
    }

    button {
      font: inherit;
    }

    button,
    a {
      touch-action: manipulation;
    }

    img {
      display: block;
      max-width: 100%;
    }

    .container {
      width: min(var(--container), calc(100% - 40px));
      margin-inline: auto;
    }

    .green {
      color: var(--green);
    }

    .eyebrow {
      display: inline-flex;
      align-items: center;
      gap: 9px;
      color: var(--green);
      font-size: 12px;
      font-weight: 800;
      letter-spacing: 2px;
      text-transform: uppercase;
    }

    .eyebrow::before {
      content: "";
      width: 7px;
      height: 7px;
      background: var(--green);
      border-radius: 50%;
      box-shadow: 0 0 12px var(--green);
    }

    .section {
      padding: 100px 0;
    }

    .section-heading {
      max-width: 650px;
      margin-bottom: 44px;
    }

    .section-heading h2 {
      margin: 15px 0;
      font-size: clamp(30px, 5vw, 48px);
      line-height: 1.12;
      letter-spacing: -1.5px;
    }

    .section-heading p {
      color: var(--muted);
      max-width: 560px;
    }

    /* =========================================
       BUTTONS
    ========================================= */

    .btn {
      display: inline-flex;
      justify-content: center;
      align-items: center;
      gap: 10px;
      min-height: 49px;
      padding: 13px 20px;
      border: 1px solid transparent;
      border-radius: 12px;
      font-size: 14px;
      font-weight: 750;
      cursor: pointer;
      transition:
        transform .2s ease,
        background .2s ease,
        border-color .2s ease,
        box-shadow .2s ease;
    }

    .btn:hover {
      transform: translateY(-2px);
    }

    .btn-primary {
      background: var(--green);
      color: #04100A;
      box-shadow: 0 0 25px rgba(54, 232, 154, .12);
    }

    .btn-primary:hover {
      background: var(--bright);
      box-shadow: 0 0 30px rgba(54, 232, 154, .23);
    }

    .btn-secondary {
      color: var(--text);
      border-color: var(--border);
      background: rgba(255,255,255,.025);
    }

    .btn-secondary:hover {
      border-color: var(--green);
      background: rgba(54,232,154,.06);
    }

    /* =========================================
       HEADER
    ========================================= */

    .header {
      position: sticky;
      top: 0;
      z-index: 100;
      background: rgba(5, 8, 6, .88);
      backdrop-filter: blur(18px);
      border-bottom: 1px solid rgba(36, 53, 43, .75);
    }

    .navbar {
      min-height: 76px;
      display: flex;
      align-items: center;
      justify-content: space-between;
      gap: 25px;
    }

    .brand {
      display: inline-flex;
      align-items: center;
      gap: 11px;
      flex-shrink: 0;
    }

    .brand-mark {
      width: 39px;
      height: 39px;
      display: grid;
      place-items: center;
      border-radius: 12px;
      background: linear-gradient(135deg, var(--green), #137D51);
      color: #031008;
      font-weight: 950;
      font-size: 20px;
      box-shadow: 0 0 25px rgba(54,232,154,.13);
    }

    .brand-name {
      font-size: 19px;
      font-weight: 850;
      letter-spacing: -.7px;
    }

    .brand-name span {
      color: var(--green);
    }

    .nav-links {
      display: flex;
      align-items: center;
      gap: 28px;
    }

    .nav-links a {
      color: var(--muted);
      font-size: 13px;
      font-weight: 650;
      transition: color .2s ease;
    }

    .nav-links a:hover,
    .nav-links a.active {
      color: var(--green);
    }

    .nav-cta {
      min-height: 42px;
      padding: 10px 16px;
    }

    .menu-toggle {
      display: none;
      width: 43px;
      height: 43px;
      border: 1px solid var(--border);
      background: var(--card);
      color: var(--text);
      border-radius: 11px;
      font-size: 23px;
      cursor: pointer;
    }

    /* =========================================
       HERO
    ========================================= */

    .hero {
      position: relative;
      min-height: 640px;
      padding: 85px 0 95px;
      overflow: hidden;
      isolation: isolate;
    }

    .hero::before {
      content: "";
      position: absolute;
      z-index: -1;
      width: 550px;
      height: 550px;
      top: -110px;
      right: -110px;
      border-radius: 50%;
      background: radial-gradient(
        circle,
        rgba(29, 177, 105, .13),
        transparent 70%
      );
      pointer-events: none;
    }

    .hero-grid {
      display: grid;
      grid-template-columns: 1.05fr .95fr;
      align-items: center;
      gap: 45px;
    }

    .hero-copy {
      position: relative;
      z-index: 2;
    }

    .hero h1 {
      margin: 23px 0;
      font-size: clamp(43px, 6.3vw, 76px);
      line-height: 1.02;
      letter-spacing: -3.5px;
      font-weight: 850;
    }

    .hero h1 .highlight {
      color: var(--green);
    }

    .hero-description {
      max-width: 510px;
      margin: 0 0 30px;
      color: var(--muted);
      font-size: 16px;
      line-height: 1.85;
    }

    .hero-actions {
      display: flex;
      flex-wrap: wrap;
      gap: 12px;
    }

    .hero-proof {
      display: flex;
      flex-wrap: wrap;
      gap: 18px;
      margin-top: 29px;
      color: var(--muted);
      font-size: 12px;
    }

    .hero-proof span::before {
      content: "✓";
      color: var(--green);
      margin-right: 7px;
      font-weight: 900;
    }

    /* =========================================
       CSS ROBOT PLACEHOLDER
       Replace later with a real 3D model.
    ========================================= */

    .robot-stage {
      position: relative;
      min-height: 450px;
      display: grid;
      place-items: center;
      isolation: isolate;
    }

    .robot-orbit {
      position: absolute;
      width: min(100%, 410px);
      aspect-ratio: 1;
      border: 1px solid rgba(54,232,154,.17);
      border-radius: 50%;
      transform: rotate(-22deg) scaleY(.72);
      box-shadow: 0 0 60px rgba(54,232,154,.035);
    }

    .robot-orbit::before,
    .robot-orbit::after {
      content: "";
      position: absolute;
      border: 1px solid rgba(54,232,154,.12);
      border-radius: 50%;
      inset: 22px;
    }

    .robot-orbit::after {
      inset: 48px;
    }

    .robot-glow {
      position: absolute;
      width: 270px;
      height: 300px;
      border-radius: 50%;
      background: rgba(34, 215, 130, .10);
      filter: blur(65px);
    }

    .robot {
      position: relative;
      z-index: 2;
      width: 215px;
      animation: robot-float 4s ease-in-out infinite;
      filter: drop-shadow(0 20px 35px rgba(0,0,0,.45));
    }

    .robot-head {
      position: relative;
      width: 174px;
      height: 145px;
      margin: 0 auto;
      border: 2px solid #47695A;
      border-radius: 46px 46px 38px 38px;
      background: linear-gradient(145deg, #D6E8DF, #829D8F 50%, #435D50);
      box-shadow:
        inset -12px -12px 20px rgba(0,0,0,.28),
        inset 8px 8px 18px rgba(255,255,255,.55),
        0 0 30px rgba(54,232,154,.12);
    }

    .robot-head::before {
      content: "";
      position: absolute;
      left: 50%;
      top: -12px;
      width: 48px;
      height: 12px;
      transform: translateX(-50%);
      border-radius: 10px 10px 0 0;
      background: #6B9B83;
    }

    .robot-face {
      position: absolute;
      inset: 23px 15px;
      display: flex;
      align-items: center;
      justify-content: center;
      gap: 24px;
      border: 1px solid rgba(54,232,154,.2);
      border-radius: 27px;
      background: linear-gradient(145deg, #06120C, #102A1C);
      box-shadow: inset 0 0 22px rgba(0,0,0,.8);
    }

    .robot-eye {
      width: 20px;
      height: 28px;
      border-radius: 50%;
      background: var(--bright);
      box-shadow: 0 0 14px rgba(117,255,184,.85);
      animation: robot-blink 5s infinite;
    }

    .robot-neck {
      width: 52px;
      height: 19px;
      margin: 0 auto;
      background: linear-gradient(90deg, #334B3D, #91B5A0, #334B3D);
    }

    .robot-body {
      position: relative;
      width: 194px;
      height: 142px;
      margin: 0 auto;
      border: 2px solid #395F4A;
      border-radius: 44px 44px 34px 34px;
      background: linear-gradient(140deg, #B7D0C2, #668875 55%, #304E3B);
      box-shadow:
        inset -10px -12px 18px rgba(0,0,0,.3),
        inset 8px 8px 18px rgba(255,255,255,.25);
    }

    .robot-core {
      position: absolute;
      top: 25px;
      left: 50%;
      width: 57px;
      height: 57px;
      transform: translateX(-50%);
      display: grid;
      place-items: center;
      border: 2px solid #63D99A;
      border-radius: 50%;
      background: #071A10;
      box-shadow: 0 0 24px rgba(54,232,154,.24);
    }

    .robot-core::before {
      content: "";
      width: 24px;
      height: 24px;
      border-radius: 50%;
      background: var(--green);
      box-shadow: 0 0 18px var(--green);
      animation: core-pulse 2s ease-in-out infinite;
    }

    .robot-arm {
      position: absolute;
      top: 29px;
      width: 25px;
      height: 82px;
      border-radius: 16px;
      border: 2px solid #456854;
      background: linear-gradient(90deg, #536E5D, #B5CCBE, #536E5D);
    }

    .robot-arm.left {
      left: -25px;
      transform: rotate(12deg);
    }

    .robot-arm.right {
      right: -25px;
      transform: rotate(-12deg);
    }

    .robot-platform {
      position: absolute;
      bottom: 13px;
      width: 230px;
      height: 30px;
      border: 1px solid rgba(54,232,154,.5);
      border-radius: 50%;
      background: rgba(54,232,154,.06);
      box-shadow: 0 0 25px rgba(54,232,154,.13);
    }

    .robot-label {
      position: absolute;
      z-index: 3;
      padding: 10px 14px;
      border: 1px solid var(--border);
      border-radius: 12px;
      background: rgba(13,21,17,.88);
      backdrop-filter: blur(10px);
      font-size: 11px;
      font-weight: 700;
      color: var(--text);
    }

    .robot-label strong {
      display: block;
      color: var(--green);
      font-size: 12px;
    }

    .label-top {
      top: 50px;
      right: 0;
      animation: label-float 4s ease-in-out infinite;
    }

    .label-bottom {
      bottom: 62px;
      left: 0;
      animation: label-float 4s ease-in-out infinite reverse;
    }

    @keyframes robot-float {
      0%, 100% { transform: translateY(0); }
      50% { transform: translateY(-13px); }
    }

    @keyframes robot-blink {
      0%, 44%, 48%, 100% {
        transform: scaleY(1);
      }
      46% {
        transform: scaleY(.08);
      }
    }

    @keyframes core-pulse {
      0%, 100% { opacity: .8; transform: scale(.9); }
      50% { opacity: 1; transform: scale(1.08); }
    }

    @keyframes label-float {
      0%, 100% { transform: translateY(0); }
      50% { transform: translateY(-7px); }
    }

    /* =========================================
       TRUST STRIP
    ========================================= */

    .trust-strip {
      border-top: 1px solid var(--border);
      border-bottom: 1px solid var(--border);
      background: rgba(255,255,255,.012);
    }

    .trust-inner {
      min-height: 83px;
      display: flex;
      align-items: center;
      justify-content: center;
      gap: 30px;
      flex-wrap: wrap;
      color: var(--muted);
      font-size: 12px;
      text-align: center;
    }

    .trust-inner strong {
      color: var(--text);
      font-weight: 750;
    }

    /* =========================================
       SERVICES
    ========================================= */

    .services-grid {
      display: grid;
      grid-template-columns: repeat(2, minmax(0, 1fr));
      gap: 20px;
    }

    .service-card {
      position: relative;
      overflow: hidden;
      padding: 30px;
      min-height: 300px;
      border: 1px solid var(--border);
      border-radius: var(--radius);
      background: linear-gradient(145deg, var(--card), #09100C);
      transition:
        transform .25s ease,
        border-color .25s ease;
    }

    .service-card:hover {
      transform: translateY(-5px);
      border-color: rgba(54,232,154,.55);
    }

    .service-card::after {
      content: "";
      position: absolute;
      width: 180px;
      height: 180px;
      right: -65px;
      top: -65px;
      border-radius: 50%;
      background: rgba(54,232,154,.06);
      filter: blur(35px);
      pointer-events: none;
    }

    .service-icon {
      width: 55px;
      height: 55px;
      display: grid;
      place-items: center;
      border-radius: 15px;
      border: 1px solid rgba(54,232,154,.25);
      background: rgba(54,232,154,.08);
      color: var(--green);
      font-size: 25px;
      font-weight: 800;
    }

    .service-card h3 {
      margin: 23px 0 10px;
      font-size: 23px;
      letter-spacing: -.5px;
    }

    .service-card p {
      color: var(--muted);
      font-size: 14px;
      max-width: 430px;
    }

    .text-link {
      display: inline-flex;
      align-items: center;
      gap: 8px;
      margin-top: 12px;
      color: var(--green);
      font-size: 13px;
      font-weight: 800;
    }

    .text-link span {
      transition: transform .2s ease;
    }

    .text-link:hover span {
      transform: translateX(5px);
    }

    /* =========================================
       PORTFOLIO
    ========================================= */

    .portfolio-section {
      background:
        radial-gradient(
          ellipse at 50% 0%,
          rgba(54,232,154,.045),
          transparent 60%
        );
    }

    .portfolio-grid {
      display: grid;
      grid-template-columns: repeat(3, minmax(0, 1fr));
      gap: 19px;
    }

    .portfolio-card {
      overflow: hidden;
      border: 1px solid var(--border);
      border-radius: 18px;
      background: var(--card);
      transition: transform .25s ease, border-color .25s ease;
    }

    .portfolio-card:hover {
      transform: translateY(-4px);
      border-color: rgba(54,232,154,.45);
    }

    .portfolio-art {
      position: relative;
      min-height: 235px;
      display: grid;
      place-items: center;
      overflow: hidden;
      isolation: isolate;
    }

    .art-one {
      background: radial-gradient(circle at 50% 40%, #29573E, #101C14 70%);
    }

    .art-two {
      background: radial-gradient(circle at 50% 40%, #263F35, #0A100D 70%);
    }

    .art-three {
      background: radial-gradient(circle at 50% 40%, #24543A, #0A100D 70%);
    }

    .art-orbit {
      position: absolute;
      z-index: -1;
      width: 175px;
      height: 175px;
      border: 1px solid rgba(117,255,184,.25);
      border-radius: 50%;
      transform: rotate(-25deg) scaleY(.65);
    }

    .art-orbit::after {
      content: "";
      position: absolute;
      inset: 22px;
      border: 1px solid rgba(117,255,184,.15);
      border-radius: 50%;
    }

    .art-product {
      position: relative;
      display: grid;
      place-items: center;
      width: 85px;
      height: 140px;
      border: 2px solid rgba(214,244,225,.8);
      border-radius: 20px 20px 14px 14px;
      background: linear-gradient(100deg, #3A6A4C, #C0D9C8 42%, #244631);
      box-shadow:
        15px 20px 35px rgba(0,0,0,.35),
        inset 5px 0 10px rgba(255,255,255,.25);
      transform: rotate(-8deg);
    }

    .art-product::before {
      content: "";
      position: absolute;
      top: -15px;
      width: 27px;
      height: 16px;
      border-radius: 5px 5px 0 0;
      background: #A7D8B7;
    }

    .art-product::after {
      content: "V";
      display: grid;
      place-items: center;
      width: 38px;
      height: 38px;
      border: 1px solid rgba(255,255,255,.45);
      border-radius: 50%;
      color: #E5FFF0;
      font-size: 21px;
      font-weight: 900;
    }

    .art-caption {
      position: absolute;
      bottom: 18px;
      left: 18px;
      right: 18px;
      color: #DDFCE9;
      font-size: 10px;
      font-weight: 800;
      letter-spacing: 2px;
      text-transform: uppercase;
    }

    .portfolio-info {
      padding: 19px;
    }

    .portfolio-info h3 {
      margin: 0 0 5px;
      font-size: 17px;
    }

    .portfolio-info p {
      margin: 0;
      color: var(--muted);
      font-size: 12px;
    }

    .portfolio-note {
      margin-top: 24px;
      color: var(--muted);
      font-size: 12px;
    }

    /* =========================================
       PROCESS
    ========================================= */

    .process-grid {
      display: grid;
      grid-template-columns: repeat(3, minmax(0, 1fr));
      gap: 20px;
    }

    .process-card {
      padding: 25px;
      border-top: 1px solid var(--border);
    }

    .process-number {
      color: var(--green);
      font-size: 12px;
      font-weight: 900;
      letter-spacing: 2px;
    }

    .process-card h3 {
      margin: 17px 0 8px;
      font-size: 20px;
    }

    .process-card p {
      color: var(--muted);
      font-size: 13px;
    }

    /* =========================================
       CONTACT CTA
    ========================================= */

    .contact-panel {
      position: relative;
      overflow: hidden;
      padding: 60px 30px;
      text-align: center;
      border: 1px solid rgba(54,232,154,.28);
      border-radius: 28px;
      background:
        radial-gradient(
          ellipse at 50% 0%,
          rgba(54,232,154,.11),
          transparent 65%
        ),
        var(--card);
    }

    .contact-panel h2 {
      max-width: 680px;
      margin: 17px auto;
      font-size: clamp(32px, 5vw, 51px);
      line-height: 1.12;
      letter-spacing: -1.7px;
    }

    .contact-panel p {
      max-width: 530px;
      margin: 0 auto 25px;
      color: var(--muted);
      font-size: 14px;
    }

    /* =========================================
       FOOTER
    ========================================= */

    .footer {
      padding: 30px 0;
      border-top: 1px solid var(--border);
    }

    .footer-inner {
      display: flex;
      justify-content: space-between;
      align-items: center;
      flex-wrap: wrap;
      gap: 18px;
    }

    .footer p {
      margin: 0;
      color: var(--muted);
      font-size: 11px;
    }

    .footer-links {
      display: flex;
      gap: 20px;
      flex-wrap: wrap;
    }

    .footer-links a {
      color: var(--muted);
      font-size: 11px;
    }

    .footer-links a:hover {
      color: var(--green);
    }

    /* =========================================
       SCROLL REVEAL
    ========================================= */

    .reveal {
      opacity: 0;
      transform: translateY(18px);
      transition: opacity .65s ease, transform .65s ease;
    }

    .reveal.visible {
      opacity: 1;
      transform: translateY(0);
    }

    /* =========================================
       RESPONSIVE DESIGN
    ========================================= */

    @media (max-width: 900px) {
      .nav-links {
        gap: 17px;
      }

      .hero {
        padding-top: 65px;
      }

      .hero-grid {
        grid-template-columns: 1fr 1fr;
        gap: 15px;
      }

      .hero h1 {
        font-size: clamp(39px, 6vw, 58px);
        letter-spacing: -2px;
      }

      .robot-stage {
        min-height: 390px;
        transform: scale(.9);
      }

      .portfolio-grid {
        grid-template-columns: repeat(2, minmax(0, 1fr));
      }
    }

    @media (max-width: 700px) {
      .container {
        width: calc(100% - 34px);
      }

      .navbar {
        min-height: 68px;
      }

      .brand-name {
        font-size: 17px;
      }

      .menu-toggle {
        display: grid;
        place-items: center;
      }

      .nav-links {
        position: absolute;
        top: 68px;
        left: 0;
        right: 0;
        display: none;
        flex-direction: column;
        align-items: stretch;
        gap: 0;
        padding: 12px 20px 20px;
        border-bottom: 1px solid var(--border);
        background: rgba(5,8,6,.98);
      }

      .nav-links.open {
        display: flex;
      }

      .nav-links a {
        padding: 13px 4px;
        border-bottom: 1px solid rgba(36,53,43,.45);
      }

      .nav-links .nav-cta {
        margin-top: 12px;
        text-align: center;
      }

      .hero {
        padding: 65px 0 45px;
      }

      .hero-grid {
        grid-template-columns: 1fr;
        gap: 20px;
      }

      .hero h1 {
        font-size: clamp(43px, 12vw, 65px);
        letter-spacing: -2.5px;
      }

      .hero-description {
        font-size: 14px;
      }

      .robot-stage {
        min-height: 360px;
        transform: none;
      }

      .robot {
        transform-origin: center;
        scale: .88;
      }

      .robot-label.label-top {
        right: 0;
        top: 35px;
      }

      .robot-label.label-bottom {
        left: 0;
        bottom: 35px;
      }

      .trust-inner {
        padding: 20px 0;
        gap: 12px 20px;
      }

      .section {
        padding: 72px 0;
      }

      .services-grid,
      .portfolio-grid,
      .process-grid {
        grid-template-columns: 1fr;
      }

      .service-card {
        min-height: auto;
        padding: 25px;
      }

      .portfolio-art {
        min-height: 255px;
      }

      .process-card {
        padding: 20px 10px;
      }

      .contact-panel {
        padding: 45px 22px;
      }

      .footer-inner {
        align-items: flex-start;
        flex-direction: column;
      }
    }

    @media (max-width: 380px) {
      .container {
        width: calc(100% - 26px);
      }

      .hero-actions {
        flex-direction: column;
      }

      .hero-actions .btn {
        width: 100%;
      }

      .robot-label {
        font-size: 10px;
      }
    }

    @media (prefers-reduced-motion: reduce) {
      *,
      *::before,
      *::after {
        scroll-behavior: auto !important;
        animation-duration: .01ms !important;
        animation-iteration-count: 1 !important;
        transition-duration: .01ms !important;
      }

      .reveal {
        opacity: 1;
        transform: none;
      }
    }
  </style>
</head>

<body>

  <!-- HEADER -->
  <header class="header">
    <div class="container navbar">

      <a class="brand" href="#home" aria-label="Veltrion AI home">
        <span class="brand-mark">V</span>
        <span class="brand-name">Veltrion <span>AI</span></span>
      </a>

      <button
        class="menu-toggle"
        id="menuToggle"
        type="button"
        aria-label="Open navigation menu"
        aria-expanded="false"
        aria-controls="navLinks">
        ☰
      </button>

      <nav class="nav-links" id="navLinks" aria-label="Main navigation">
        <a href="#home">Home</a>
        <a href="#services">Services</a>
        <a href="#portfolio">Portfolio</a>
        <a href="#process">Our Process</a>
        <a href="#contact" class="btn btn-primary nav-cta">
          Let's Talk ↗
        </a>
      </nav>

    </div>
  </header>

  <main>

    <!-- HERO -->
    <section class="hero" id="home">
      <div class="container hero-grid">

        <div class="hero-copy">

          <span class="eyebrow">Next-Generation Creative Studio</span>

          <h1>
            Your Products.<br>
            Our Creativity.<br>
            <span class="highlight">Powered by AI.</span>
          </h1>

          <p class="hero-description">
            We transform product ideas into premium visual advertisements
            using AI-powered creativity. Make your brand stand out with
            compelling image ads and cinematic video ads.
          </p>

          <div class="hero-actions">
            <a href="#services" class="btn btn-primary">
              Explore Our Services ↗
            </a>

            <a href="#portfolio" class="btn btn-secondary">
              View Portfolio →
            </a>
          </div>

          <div class="hero-proof">
            <span>Creative Visuals</span>
            <span>AI-Powered Workflow</span>
            <span>Brand-Focused Design</span>
          </div>

        </div>

        <!-- Animated robot illustration -->
        <div class="robot-stage" aria-label="Animated robot illustration">

          <div class="robot-glow"></div>
          <div class="robot-orbit"></div>

          <div class="robot-label label-top">
            <strong>AI CREATIVE</strong>
            Intelligent Visuals
          </div>

          <div class="robot" aria-hidden="true">

            <div class="robot-head">
              <div class="robot-face">
                <span class="robot-eye"></span>
                <span class="robot-eye"></span>
              </div>
            </div>

            <div class="robot-neck"></div>

            <div class="robot-body">
              <div class="robot-arm left"></div>
              <div class="robot-arm right"></div>
              <div class="robot-core"></div>
            </div>

          </div>

          <div class="robot-platform"></div>

          <div class="robot-label label-bottom">
            <strong>VELTRION AI</strong>
            Intelligence. Innovation.
          </div>

        </div>

      </div>
    </section>

    <!-- TRUST STRIP -->
    <section class="trust-strip" aria-label="Our capabilities">
      <div class="container trust-inner">
        <strong>CREATIVE THINKING</strong>
        <span>✦</span>
        <strong>AI-POWERED DESIGN</strong>
        <span>✦</span>
        <strong>VISUAL STORYTELLING</strong>
      </div>
    </section>

    <!-- SERVICES -->
    <section class="section" id="services">
      <div class="container">

        <div class="section-heading reveal">
          <span class="eyebrow">What We Create</span>

          <h2>
            Creative Ads.<br>
            <span class="green">Built for Your Brand.</span>
          </h2>

          <p>
            Two focused services to help businesses present their products
            with stronger visuals and more engaging creative content.
          </p>
        </div>

        <div class="services-grid">

          <article class="service-card reveal">
            <div class="service-icon" aria-hidden="true">▧</div>

            <h3>AI Image Ads</h3>

            <p>
              Premium product visuals, advertising posters and campaign
              creatives designed to make your products look distinctive
              and professional.
            </p>

            <a class="text-link" href="#contact">
              Discuss an Image Ad <span>→</span>
            </a>
          </article>

          <article class="service-card reveal">
            <div class="service-icon" aria-hidden="true">▶</div>

            <h3>AI Video Ads</h3>

            <p>
              Engaging AI-assisted product videos with cinematic motion,
              creative storytelling and a visual direction tailored
              to your brand.
            </p>

            <a class="text-link" href="#contact">
              Discuss a Video Ad <span>→</span>
            </a>
          </article>

        </div>
      </div>
    </section>

    <!-- PORTFOLIO -->
    <section class="section portfolio-section" id="portfolio">
      <div class="container">

        <div class="section-heading reveal">
          <span class="eyebrow">Selected Concepts</span>

          <h2>
            Creativity You<br>
            <span class="green">Can See.</span>
          </h2>

          <p>
            Explore the visual direction of our product advertising.
            These initial design concepts are placeholders that will
            be replaced with our actual portfolio work.
          </p>
        </div>

        <div class="portfolio-grid">

          <article class="portfolio-card reveal">
            <div class="portfolio-art art-one">
              <div class="art-orbit"></div>
              <div class="art-product"></div>
              <span class="art-caption">Premium Product Concept</span>
            </div>

            <div class="portfolio-info">
              <h3>Product Visuals</h3>
              <p>AI Image Ads · Concept Preview</p>
            </div>
          </article>

          <article class="portfolio-card reveal">
            <div class="portfolio-art art-two">
              <div class="art-orbit"></div>
              <div class="art-product"></div>
              <span class="art-caption">Creative Campaign Concept</span>
            </div>

            <div class="portfolio-info">
              <h3>Brand Campaign</h3>
              <p>Advertising Design · Concept Preview</p>
            </div>
          </article>

          <article class="portfolio-card reveal">
            <div class="portfolio-art art-three">
              <div class="art-orbit"></div>
              <div class="art-product"></div>
              <span class="art-caption">Cinematic Visual Concept</span>
            </div>

            <div class="portfolio-info">
              <h3>Video Ad Direction</h3>
              <p>AI Video Ads · Concept Preview</p>
            </div>
          </article>

        </div>

        <p class="portfolio-note reveal">
          Note: These are CSS-generated visual placeholders, not completed
          client projects. Actual portfolio images and videos will be
          added before the public launch.
        </p>

      </div>
    </section>

    <!-- PROCESS -->
    <section class="section" id="process">
      <div class="container">

        <div class="section-heading reveal">
          <span class="eyebrow">How We Work</span>

          <h2>
            From Product<br>
            <span class="green">to Creative.</span>
          </h2>

          <p>
            A simple, clear workflow designed to make the creative
            process easy for our customers.
          </p>
        </div>

        <div class="process-grid">

          <article class="process-card reveal">
            <span class="process-number">STEP 01</span>
            <h3>Share Your Product</h3>
            <p>
              Tell us about your product, target audience and the kind
              of advertisement you want.
            </p>
          </article>

          <article class="process-card reveal">
            <span class="process-number">STEP 02</span>
            <h3>Creative Production</h3>
            <p>
              We develop the creative direction and produce your
              advertisement according to the agreed requirements.
            </p>
          </article>

          <article class="process-card reveal">
            <span class="process-number">STEP 03</span>
            <h3>Review & Delivery</h3>
            <p>
              Review the agreed deliverable and receive the final
              creative according to the project terms.
            </p>
          </article>

        </div>
      </div>
    </section>

    <!-- CONTACT -->
    <section class="section" id="contact">
      <div class="container">

        <div class="contact-panel reveal">

          <span class="eyebrow">Let's Create Something</span>

          <h2>
            Your Next Great Ad<br>
            <span class="green">Starts Here.</span>
          </h2>

          <p>
            Have a product to promote? Get in touch with Veltrion AI
            to discuss your image ad or video ad requirements.
          </p>

          <a href="#services" class="btn btn-primary">
            Explore Services ↗
          </a>

        </div>

      </div>
    </section>

  </main>

  <!-- FOOTER -->
  <footer class="footer">
    <div class="container footer-inner">

      <a class="brand" href="#home" aria-label="Veltrion AI home">
        <span class="brand-mark">V</span>
        <span class="brand-name">Veltrion <span>AI</span></span>
      </a>

      <p>
        © <span id="currentYear"></span> Veltrion AI.
        Creative intelligence for modern brands.
      </p>

      <div class="footer-links">
        <a href="#home">Home</a>
        <a href="#services">Services</a>
        <a href="#portfolio">Portfolio</a>
        <a href="#contact">Contact</a>
      </div>

    </div>
  </footer>

  <script>
    "use strict";

    /* =========================================
       MOBILE NAVIGATION
    ========================================= */

    const menuToggle = document.getElementById("menuToggle");
    const navLinks = document.getElementById("navLinks");

    menuToggle.addEventListener("click", () => {
      const isOpen = navLinks.classList.toggle("open");

      menuToggle.setAttribute("aria-expanded", String(isOpen));
      menuToggle.setAttribute(
        "aria-label",
        isOpen ? "Close navigation menu" : "Open navigation menu"
      );

      menuToggle.textContent = isOpen ? "×" : "☰";
    });

    navLinks.querySelectorAll("a").forEach((link) => {
      link.addEventListener("click", () => {
        navLinks.classList.remove("open");
        menuToggle.setAttribute("aria-expanded", "false");
        menuToggle.setAttribute("aria-label", "Open navigation menu");
        menuToggle.textContent = "☰";
      });
    });

    /* =========================================
       CURRENT YEAR
    ========================================= */

    document.getElementById("currentYear").textContent =
      new Date().getFullYear();

    /* =========================================
       SCROLL REVEAL
    ========================================= */

    const revealElements = document.querySelectorAll(".reveal");

    if ("IntersectionObserver" in window) {
      const revealObserver = new IntersectionObserver(
        (entries, observer) => {
          entries.forEach((entry) => {
            if (entry.isIntersecting) {
              entry.target.classList.add("visible");
              observer.unobserve(entry.target);
            }
          });
        },
        {
          threshold: 0.12
        }
      );

      revealElements.forEach((element) => {
        revealObserver.observe(element);
      });
    } else {
      revealElements.forEach((element) => {
        element.classList.add("visible");
      });
    }

    /* =========================================
       ACTIVE NAVIGATION LINK
    ========================================= */

    const sections = document.querySelectorAll("main section[id]");
    const navAnchors = document.querySelectorAll(
      '.nav-links a[href^="#"]'
    );

    if ("IntersectionObserver" in window) {
      const sectionObserver = new IntersectionObserver(
        (entries) => {
          entries.forEach((entry) => {
            if (entry.isIntersecting) {
              navAnchors.forEach((link) => {
                const matches =
                  link.getAttribute("href") === "#" + entry.target.id;

                link.classList.toggle("active", matches);
              });
            }
          });
        },
        {
          rootMargin: "-25% 0px -60% 0px"
        }
      );

      sections.forEach((section) => {
        sectionObserver.observe(section);
      });
    }
  </script>

</body>
</html>

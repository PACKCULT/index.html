<!DOCTYPE html>
<html lang="th">

<head>

  <meta charset="UTF-8">

  <meta
    name="viewport"
    content="width=device-width, initial-scale=1.0"
  >

  <meta
    name="theme-color"
    content="#030308"
  >

  <meta
    name="description"
    content="PACKCULT SHOP — Streetwear • Culture • Attitude"
  >

  <title>PACKCULT SHOP</title>


  <!-- GOOGLE FONT -->

  <link
    rel="preconnect"
    href="https://fonts.googleapis.com"
  >

  <link
    rel="preconnect"
    href="https://fonts.gstatic.com"
    crossorigin
  >

  <link
    href="https://fonts.googleapis.com/css2?family=Orbitron:wght@500;600;700;800;900&family=Prompt:wght@300;400;500;600;700&display=swap"
    rel="stylesheet"
  >


  <style>

    /* =====================================
       RESET
    ===================================== */

    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }


    /* =====================================
       VARIABLES
    ===================================== */

    :root {

      --cyan: #00eaff;

      --purple: #a855ff;

      --pink: #ff36d1;

      --green: #00ff9d;

      --white: #ffffff;

      --muted: #9da3b5;

      --background: #030308;

    }


    /* =====================================
       BODY
    ===================================== */

    body {

      min-height: 100vh;

      overflow-x: hidden;

      color: var(--white);

      font-family: "Prompt", sans-serif;

      background:

        radial-gradient(
          circle at 15% 20%,
          rgba(0, 234, 255, 0.16),
          transparent 28%
        ),

        radial-gradient(
          circle at 85% 25%,
          rgba(168, 85, 255, 0.20),
          transparent 30%
        ),

        radial-gradient(
          circle at 50% 90%,
          rgba(255, 54, 209, 0.12),
          transparent 30%
        ),

        var(--background);

    }


    /* =====================================
       GRID BACKGROUND
    ===================================== */

    body::before {

      content: "";

      position: fixed;

      inset: 0;

      pointer-events: none;

      z-index: 0;

      background-image:

        linear-gradient(
          rgba(0, 234, 255, 0.045) 1px,
          transparent 1px
        ),

        linear-gradient(
          90deg,
          rgba(0, 234, 255, 0.045) 1px,
          transparent 1px
        );

      background-size: 45px 45px;

      mask-image:
        linear-gradient(
          to bottom,
          black,
          transparent 90%
        );

      -webkit-mask-image:
        linear-gradient(
          to bottom,
          black,
          transparent 90%
        );

    }


    /* =====================================
       BACKGROUND GLOW
    ===================================== */

    .glow {

      position: fixed;

      width: 400px;

      height: 400px;

      border-radius: 50%;

      filter: blur(100px);

      opacity: 0.15;

      pointer-events: none;

      z-index: 0;

    }


    .glow.one {

      background: var(--cyan);

      top: -150px;

      left: -150px;

    }


    .glow.two {

      background: var(--purple);

      right: -150px;

      top: 30%;

    }


    .glow.three {

      background: var(--pink);

      bottom: -200px;

      left: 35%;

    }


    /* =====================================
       PARTICLES
    ===================================== */

    .particles {

      position: fixed;

      inset: 0;

      overflow: hidden;

      pointer-events: none;

      z-index: 1;

    }


    .particle {

      position: absolute;

      width: 3px;

      height: 3px;

      border-radius: 50%;

      background: var(--cyan);

      box-shadow:
        0 0 12px var(--cyan);

      animation:
        float linear infinite;

    }


    .particle:nth-child(1) {

      left: 8%;

      animation-duration: 7s;

      animation-delay: -2s;

    }


    .particle:nth-child(2) {

      left: 22%;

      background: var(--purple);

      box-shadow:
        0 0 12px var(--purple);

      animation-duration: 9s;

      animation-delay: -5s;

    }


    .particle:nth-child(3) {

      left: 39%;

      animation-duration: 6s;

      animation-delay: -1s;

    }


    .particle:nth-child(4) {

      left: 55%;

      background: var(--pink);

      box-shadow:
        0 0 12px var(--pink);

      animation-duration: 8s;

      animation-delay: -4s;

    }


    .particle:nth-child(5) {

      left: 73%;

      background: var(--green);

      box-shadow:
        0 0 12px var(--green);

      animation-duration: 10s;

      animation-delay: -7s;

    }


    .particle:nth-child(6) {

      left: 91%;

      animation-duration: 7s;

      animation-delay: -3s;

    }


    @keyframes float {

      from {

        transform:
          translateY(110vh);

        opacity: 0;

      }

      15% {

        opacity: 1;

      }

      85% {

        opacity: 1;

      }

      to {

        transform:
          translateY(-20vh);

        opacity: 0;

      }

    }


    /* =====================================
       CONTAINER
    ===================================== */

    .container {

      position: relative;

      z-index: 2;

      width: min(900px, 92%);

      margin: auto;

      padding:
        35px 0 50px;

    }


    /* =====================================
       ONLINE STATUS
    ===================================== */

    .status {

      display: flex;

      justify-content: center;

      align-items: center;

      gap: 8px;

      margin-bottom: 25px;

      color: #9cfaff;

      font-size: 10px;

      letter-spacing: 4px;

    }


    .status-dot {

      width: 7px;

      height: 7px;

      border-radius: 50%;

      background: var(--green);

      box-shadow:
        0 0 15px var(--green);

      animation:
        blink 1.2s infinite alternate;

    }


    @keyframes blink {

      from {
        opacity: 0.3;
      }

      to {
        opacity: 1;
      }

    }


    /* =====================================
       HERO
    ===================================== */

    .hero {

      text-align: center;

      padding:
        30px 10px 35px;

    }


    /* =====================================
       BADGE
    ===================================== */

    .badge {

      display: inline-block;

      padding:
        8px 15px;

      border:
        1px solid
        rgba(0, 234, 255, 0.35);

      border-radius: 999px;

      background:
        rgba(0, 234, 255, 0.05);

      color: #a5f8ff;

      font-size: 10px;

      letter-spacing: 3px;

      box-shadow:

        0 0 25px
        rgba(0, 234, 255, 0.08),

        inset 0 0 15px
        rgba(0, 234, 255, 0.04);

    }


    /* =====================================
       BRAND
       
       รูปโลโก้ + PACKCULT SHOP
    ===================================== */

    .brand {

      display: flex;

      justify-content: center;

      align-items: center;

      gap: 20px;

      margin:
        30px auto 20px;

    }


    /* =====================================
       LOGO
    ===================================== */

    .brand-logo {

      display: block;

      width: 130px;

      height: auto;

      object-fit: contain;

      filter:

        drop-shadow(
          0 0 10px
          rgba(0, 234, 255, 0.25)
        )

        drop-shadow(
          0 0 25px
          rgba(168, 85, 255, 0.15)
        );

      transition:
        transform 0.35s ease,
        filter 0.35s ease;

    }


    .brand-logo:hover {

      transform:
        scale(1.05);

      filter:

        drop-shadow(
          0 0 15px
          rgba(0, 234, 255, 0.5)
        )

        drop-shadow(
          0 0 30px
          rgba(168, 85, 255, 0.3)
        );

    }


    /* =====================================
       PACKCULT SHOP TEXT
    ===================================== */

    .brand-text {

      font-family:
        "Orbitron",
        sans-serif;

      font-size:
        clamp(24px, 5vw, 48px);

      font-weight: 900;

      letter-spacing: 3px;

      color: white;

      white-space: nowrap;

      text-shadow:

        0 0 8px
        var(--cyan),

        0 0 20px
        rgba(0, 234, 255, 0.5);

      animation:
        textGlow 3s ease-in-out infinite alternate;

    }


    @keyframes textGlow {

      from {

        text-shadow:

          0 0 5px
          var(--cyan),

          0 0 15px
          rgba(0, 234, 255, 0.3);

      }

      to {

        text-shadow:

          0 0 10px
          var(--cyan),

          0 0 30px
          rgba(0, 234, 255, 0.7),

          0 0 50px
          rgba(168, 85, 255, 0.25);

      }

    }


    /* =====================================
       SUBTITLE
    ===================================== */

    .subtitle {

      margin-top: 15px;

      color: var(--muted);

      font-size: 12px;

      letter-spacing: 3px;

    }


    /* =====================================
       QUOTE
    ===================================== */

    .quote {

      margin:
        25px auto 0;

      max-width: 650px;

      font-family:
        "Orbitron",
        sans-serif;

      font-size:
        clamp(14px, 3vw, 21px);

      line-height: 1.6;

      color: #f5f7ff;

      text-shadow:
        0 0 20px
        rgba(0, 234, 255, 0.15);

    }


    .quote span {

      color: var(--cyan);

      text-shadow:
        0 0 15px
        rgba(0, 234, 255, 0.7);

    }


    /* =====================================
       SOCIAL LINKS
    ===================================== */

    .links {

      display: grid;

      gap: 16px;

      width:
        min(650px, 100%);

      margin: auto;

    }


    .social-card {

      position: relative;

      display: flex;

      align-items: center;

      gap: 16px;

      padding:
        18px 20px;

      color: white;

      text-decoration: none;

      border:
        1px solid
        rgba(255,255,255,0.12);

      border-radius: 20px;

      background:

        linear-gradient(
          135deg,
          rgba(255,255,255,0.08),
          rgba(255,255,255,0.025)
        );

      backdrop-filter:
        blur(15px);

      -webkit-backdrop-filter:
        blur(15px);

      overflow: hidden;

      transition:

        transform 0.3s ease,

        border 0.3s ease,

        box-shadow 0.3s ease;

    }


    .social-card::before {

      content: "";

      position: absolute;

      width: 200%;

      height: 2px;

      left: -200%;

      top: 0;

      background:

        linear-gradient(
          90deg,
          transparent,
          var(--cyan),
          var(--purple),
          transparent
        );

      transition:
        left 0.5s ease;

    }


    .social-card:hover::before {

      left: 100%;

    }


    .social-card:hover {

      transform:
        translateY(-5px)
        scale(1.015);

      border-color:
        rgba(0,234,255,0.5);

      box-shadow:

        0 0 30px
        rgba(0,234,255,0.13),

        inset 0 0 30px
        rgba(0,234,255,0.035);

    }


    .social-card.instagram:hover {

      border-color:
        rgba(255,54,209,0.5);

      box-shadow:

        0 0 30px
        rgba(255,54,209,0.13);

    }


    /* =====================================
       SOCIAL ICON
    ===================================== */

    .icon {

      display: grid;

      place-items: center;

      width: 52px;

      height: 52px;

      flex-shrink: 0;

      border-radius: 16px;

      font-family: Arial, sans-serif;

      font-size: 25px;

      font-weight: bold;

      color: var(--cyan);

      background:
        rgba(0,234,255,0.08);

      border:
        1px solid
        rgba(0,234,255,0.25);

      box-shadow:

        inset 0 0 20px
        rgba(0,234,255,0.06),

        0 0 20px
        rgba(0,234,255,0.05);

    }


    .instagram .icon {

      color: #ff55d8;

      background:
        rgba(255,54,209,0.08);

      border-color:
        rgba(255,54,209,0.3);

      box-shadow:

        inset 0 0 20px
        rgba(255,54,209,0.06),

        0 0 20px
        rgba(255,54,209,0.05);

    }


    /* =====================================
       SOCIAL INFO
    ===================================== */

    .social-info {

      flex: 1;

    }


    .social-info strong {

      display: block;

      font-family:
        "Orbitron",
        sans-serif;

      font-size: 14px;

      letter-spacing: 1px;

    }


    .social-info small {

      display: block;

      margin-top: 4px;

      color: #8d94a8;

      font-size: 11px;

    }


    /* =====================================
       ARROW
    ===================================== */

    .arrow {

      color: var(--cyan);

      font-size: 23px;

      transition:
        transform 0.3s ease;

    }


    .instagram .arrow {

      color: #ff55d8;

    }


    .social-card:hover .arrow {

      transform:
        translate(4px,-4px);

    }


    /* =====================================
       TIKTOK
    ===================================== */

    .coming-soon {

      position: relative;

      width:
        min(650px,100%);

      margin:
        45px auto 0;

      padding:
        30px 20px;

      text-align: center;

      overflow: hidden;

      border-radius: 24px;

      border:
        1px solid
        rgba(168,85,255,0.35);

      background:

        linear-gradient(
          135deg,
          rgba(168,85,255,0.13),
          rgba(0,234,255,0.045)
        );

      box-shadow:

        0 0 45px
        rgba(168,85,255,0.08);

    }


    .coming-soon::before {

      content: "";

      position: absolute;

      width: 180px;

      height: 180px;

      right: -90px;

      top: -100px;

      border-radius: 50%;

      background:
        var(--purple);

      filter:
        blur(70px);

      opacity: 0.2;

    }


    .coming-soon h2 {

      position: relative;

      font-family:
        "Orbitron",
        sans-serif;

      font-size: 23px;

      letter-spacing: 4px;

      text-shadow:
        0 0 20px
        rgba(168,85,255,0.5);

    }


    .coming-soon p {

      position: relative;

      margin-top: 9px;

      color: #aeb5c7;

      font-size: 13px;

    }


    .soon-badge {

      display: inline-block;

      margin-top: 15px;

      padding:
        7px 13px;

      border-radius: 999px;

      border:
        1px solid
        rgba(168,85,255,0.45);

      color: #d7b8ff;

      font-size: 9px;

      letter-spacing: 3px;

      animation:
        soonGlow 2s infinite alternate;

    }


    @keyframes soonGlow {

      from {

        box-shadow:
          0 0 5px
          rgba(168,85,255,0.1);

      }

      to {

        box-shadow:
          0 0 20px
          rgba(168,85,255,0.35);

      }

    }


    /* =====================================
       FOOTER
    ===================================== */

    footer {

      margin-top: 35px;

      text-align: center;

      color: #60677a;

      font-size: 9px;

      letter-spacing: 3px;

    }


    /* =====================================
       MOBILE
    ===================================== */

    @media (max-width: 600px) {

      .container {

        width: 92%;

        padding-top: 22px;

      }


      .hero {

        padding-top: 25px;

      }


      .brand {

        gap: 12px;

        margin-top: 25px;

      }


      .brand-logo {

        width: 90px;

      }


      .brand-text {

        font-size: 21px;

        letter-spacing: 1.5px;

      }


      .subtitle {

        font-size: 9px;

        letter-spacing: 2px;

      }


      .social-card {

        padding: 15px;

        border-radius: 17px;

      }


      .icon {

        width: 47px;

        height: 47px;

        border-radius: 14px;

      }


      .social-info strong {

        font-size: 12px;

      }


      .social-info small {

        font-size: 10px;

      }


      .arrow {

        font-size: 20px;

      }


      .coming-soon {

        margin-top: 35px;

      }


      .coming-soon h2 {

        font-size: 19px;

      }

    }


    /* =====================================
       SMALL MOBILE
    ===================================== */

    @media (max-width: 380px) {

      .brand {

        gap: 8px;

      }


      .brand-logo {

        width: 75px;

      }


      .brand-text {

        font-size: 17px;

        letter-spacing: 1px;

      }


      .badge {

        font-size: 8px;

        letter-spacing: 2px;

      }


      .quote {

        font-size: 13px;

      }

    }


    /* =====================================
       REDUCE MOTION
    ===================================== */

    @media (prefers-reduced-motion: reduce) {

      * {

        animation-duration:
          0.01ms !important;

        animation-iteration-count:
          1 !important;

        scroll-behavior:
          auto !important;

        transition-duration:
          0.01ms !important;

      }

    }

  </style>

</head>


<body>


  <!-- ===================================
       BACKGROUND
  ==================================== -->

  <div class="glow one"></div>

  <div class="glow two"></div>

  <div class="glow three"></div>


  <!-- ===================================
       PARTICLES
  ==================================== -->

  <div class="particles">

    <span class="particle"></span>

    <span class="particle"></span>

    <span class="particle"></span>

    <span class="particle"></span>

    <span class="particle"></span>

    <span class="particle"></span>

  </div>


  <!-- ===================================
       MAIN
  ==================================== -->

  <main class="container">


    <!-- ONLINE -->

    <div class="status">

      <span class="status-dot"></span>

      PACKCULT ONLINE

    </div>


    <!-- =================================
         HERO
    ================================== -->

    <section class="hero">


      <div class="badge">

        STREETWEAR
        •
        CULTURE
        •
        ATTITUDE

      </div>


      <!-- =================================
           LOGO + TEXT

           รูปโลโก้ของคุณอยู่ซ้าย
           PACKCULT SHOP อยู่ขวา
      ================================== -->

      <div class="brand">


        <!--
          เปลี่ยน logo.png
          เป็นชื่อไฟล์รูปโลโก้ของคุณ
        -->

        <img
          class="brand-logo"
          src="logo.png"
          alt="PACKCULT Logo"
        >


        <div class="brand-text">

          PACKCULT SHOP

        </div>


      </div>


      <!-- SUBTITLE -->

      <p class="subtitle">

        WEAR YOUR ATTITUDE.
        BUILD YOUR CULTURE.

      </p>


      <!-- QUOTE -->

      <p class="quote">

        “
        <span>
          Wear what you believe.
        </span>

        <br>

        Make your own culture.

        ”

      </p>


    </section>


    <!-- =================================
         SOCIAL
    ================================== -->

    <section class="links">


      <!-- FACEBOOK -->

      <a
        class="social-card"
        href="https://www.facebook.com/share/18ZmcmhnFq/"
        target="_blank"
        rel="noopener noreferrer"
      >


        <div class="icon">

          f

        </div>


        <div class="social-info">

          <strong>

            FACEBOOK

          </strong>


          <small>

            ติดตาม PACKCULT SHOP

          </small>

        </div>


        <div class="arrow">

          ↗

        </div>


      </a>


      <!-- INSTAGRAM -->

      <a
        class="social-card instagram"
        href="https://www.instagram.com/packcult.shop?igsh=ZDZybXI4cXV6ZGNs"
        target="_blank"
        rel="noopener noreferrer"
      >


        <div class="icon">

          ◎

        </div>


        <div class="social-info">

          <strong>

            INSTAGRAM

          </strong>


          <small>

            @packcult.shop

          </small>

        </div>


      

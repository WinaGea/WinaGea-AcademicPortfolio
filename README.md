<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Wina Gea | Portfolio</title>
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@400;500;600;700&display=swap" rel="stylesheet">
  <style>
    :root {
      --bg: #1a1a1a;
      --purple1: #8d5cf6;
      --purple2: #a36ff7;
      --white: #ffffff;
      --text: rgba(255,255,255,.75);
      --card: rgba(255, 255, 255, 0.06);
    }
    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
      font-family: "Poppins", sans-serif;
    }
    body {
      background: radial-gradient(circle at top, #a36ff7 0%, #6d34b6 45%, #1b122b 100%);
      min-height: 100vh;
      color: var(--white);
    }
    /* NAVBAR */
    .navbar {
      width: 100%;
      padding: 18px 7%;
      display: flex;
      align-items: center;
      justify-content: space-between;
      position: fixed;
      top: 0;
      left: 0;
      z-index: 50;
      background: rgba(6, 6, 6, 0.6);
      backdrop-filter: blur(10px);
      border-bottom: 1px solid rgba(255,255,255,0.04);
    }
    .logo {
      font-size: 1.1rem;
      font-weight: 600;
      letter-spacing: 2px;
    }
    .nav-links {
      display: flex;
      gap: 28px;
    }
    .nav-links a {
      color: #fff;
      font-size: .9rem;
      text-decoration: none;
      transition: .2s;
    }
    .nav-links a:hover,
    .nav-links a.active {
      color: #ffe9ff;
    }

    /* HERO */
    .hero {
      display: grid;
      grid-template-columns: 1.05fr .95fr;
      gap: 30px;
      padding: 140px 7% 60px;
      align-items: center;
      min-height: 100vh;
    }
    .hero-left small {
      background: rgba(255,255,255,0.09);
      padding: 7px 18px;
      border-radius: 999px;
      font-size: .7rem;
      display: inline-flex;
      gap: 6px;
      align-items: center;
      margin-bottom: 16px;
    }
    .hero-left h1 {
      font-size: clamp(2.6rem, 4vw, 3.4rem);
      font-weight: 700;
      line-height: 1.1;
      margin-bottom: 12px;
    }
    .hero-left h1 span {
      display: block;
    }
    .hero-left .role {
      font-size: 1rem;
      color: rgba(255,255,255,.75);
      margin-bottom: 18px;
    }
    .hero-left p {
      max-width: 520px;
      font-size: .9rem;
      line-height: 1.5;
      color: rgba(255,255,255,.85);
    }
    .hero-buttons {
      margin-top: 28px;
      display: flex;
      gap: 14px;
      flex-wrap: wrap;
    }
    .btn-primary {
      background: #fff;
      color: #2c1e42;
      border: none;
      padding: 12px 26px;
      border-radius: 999px;
      font-weight: 600;
      cursor: pointer;
      transition: .2s;
    }
    .btn-primary:hover {
      transform: translateY(-2px);
    }
    .btn-secondary {
      background: transparent;
      border: 1px solid rgba(255,255,255,.5);
      color: #fff;
      padding: 12px 26px;
      border-radius: 999px;
      font-weight: 500;
      cursor: pointer;
      transition: .2s;
    }
    .btn-secondary:hover {
      background: rgba(255,255,255,.1);
    }
    /* SOCIAL */
    .social-row {
      display: flex;
      gap: 14px;
      margin-top: 30px;
      align-items: center;
    }
    .social-row a {
      width: 40px;
      height: 40px;
      border-radius: 50%;
      border: 1px solid rgba(255,255,255,.35);
      display: flex;
      align-items: center;
      justify-content: center;
      text-decoration: none;
      color: #fff;
      font-size: .85rem;
      transition: .2s;
    }
    .social-row a:hover {
      background: rgba(255,255,255,.15);
    }

    /* HERO RIGHT */
    .hero-right {
      display: flex;
      justify-content: center;
    }
    .profile-wrapper {
      background: radial-gradient(circle, rgba(255,255,255,.06), rgba(255,255,255,0));
      border-radius: 48% 52% 46% 54%;
      width: clamp(300px, 30vw, 400px);
      aspect-ratio: 1/1;
      display: grid;
      place-items: center;
      position: relative;
      box-shadow: 0 20px 60px rgba(0,0,0,.25);
    }
    .profile-wrapper::after {
      content: "";
      position: absolute;
      inset: -35px;
      border: 1px solid rgba(255,255,255,.14);
      border-radius: inherit;
      z-index: 0;
    }
    .profile-img {
      width: 68%;
      aspect-ratio: 1/1;
      border-radius: 50%;
      background: url("https://images.unsplash.com/photo-1525130413817-d45c1d127c42?q=80&w=600&auto=format&fit=crop") center/cover no-repeat;
      border: 5px solid rgba(255,255,255,.75);
      z-index: 2;
      box-shadow: 0 20px 40px rgba(0,0,0,.25);
    }

    /* RESPONSIVE */
    @media (max-width: 980px) {
      .hero {
        grid-template-columns: 1fr;
        text-align: left;
      }
      .hero-right {
        justify-content: flex-start;
      }
      .profile-wrapper {
        margin-top: 20px;
      }
      .nav-links {
        gap: 16px;
      }
    }
    @media (max-width: 640px) {
      .navbar {
        padding: 16px 5%;
      }
      .hero {
        padding-inline: 5%;
      }
      .hero-left h1 {
        font-size: 2.45rem;
      }
      .hero-buttons {
        flex-direction: column;
        align-items: flex-start;
      }
      .social-row {
        gap: 10px;
      }
    }
  </style>
</head>
<body>

  <!-- NAVBAR -->
  <header class="navbar">
    <div class="logo">WG</div>
    <nav class="nav-links">
      <a href="#home" class="active">Home</a>
      <a href="#projects">Projects</a>
      <a href="#about">About</a>
      <a href="#contact">Contact</a>
    </nav>
  </header>

  <!-- HERO -->
  <section class="hero" id="home">
    <div class="hero-left">
      <small>👋 Welcome to my portfolio</small>
      <h1>I'm <span>Wina Gea</span></h1>
      <div class="role">Computer Technology Student &amp; IoT Enthusiast</div>
      <p>
        I enjoy building IoT prototypes, designing clean user interfaces, and working with
        database-driven applications. Here are some of the projects I’ve built during my study.
      </p>
      <div class="hero-buttons">
        <button class="btn-primary">Let’s Connect</button>
        <button class="btn-secondary" onclick="window.location='#projects'">View Projects</button>
      </div>
      <div class="social-row">
        <a href="mailto:winagea22@gmail.com">✉</a>
        <a href="https://wa.me/628xxxxxxxxxx" target="_blank">WA</a>
        <a href="https://linkedin.com/in/winagea" target="_blank">in</a>
        <a href="https://github.com/winagea" target="_blank">🐱</a>
      </div>
    </div>

    <div class="hero-right">
      <div class="profile-wrapper">
        <!-- ganti URL foto di .profile-img di CSS ya -->
        <div class="profile-img"></div>
      </div>
    </div>
  </section>

</body>
</html>

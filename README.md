<!DOCTYPE html>
<html lang="th">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<meta name="theme-color" content="#050507">
<title>PACKCULT SHOP</title>

<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Orbitron:wght@600;700;800;900&family=Prompt:wght@400;500;600;700&display=swap" rel="stylesheet">

<style>
*{box-sizing:border-box;margin:0;padding:0}

:root{
  --cyan:#00eaff;
  --purple:#a855ff;
  --pink:#ff36d1;
  --green:#00ff9d;
  --bg:#050507;
  --muted:#a0a5b5;
}

html{
  scroll-behavior:smooth;
}

body{
  min-height:100vh;
  overflow-x:hidden;
  color:#fff;
  font-family:"Prompt",sans-serif;
  background:
    radial-gradient(circle at 15% 10%,rgba(0,234,255,.15),transparent 30%),
    radial-gradient(circle at 85% 20%,rgba(168,85,255,.18),transparent 32%),
    radial-gradient(circle at 50% 100%,rgba(255,54,209,.12),transparent 35%),
    var(--bg);
}

body:before{
  content:"";
  position:fixed;
  inset:0;
  z-index:0;
  pointer-events:none;

  background-image:
    linear-gradient(rgba(0,234,255,.045) 1px,transparent 1px),
    linear-gradient(90deg,rgba(0,234,255,.045) 1px,transparent 1px);

  background-size:45px 45px;

  mask-image:linear-gradient(to bottom,#000,transparent 92%);
  -webkit-mask-image:linear-gradient(to bottom,#000,transparent 92%);
}

/* GLOW */

.glow{
  position:fixed;
  width:380px;
  height:380px;
  border-radius:50%;
  filter:blur(100px);
  opacity:.14;
  pointer-events:none;
  z-index:0;
}

.one{
  background:var(--cyan);
  top:-170px;
  left:-170px;
}

.two{
  background:var(--purple);
  right:-170px;
  top:30%;
}

.three{
  background:var(--pink);
  bottom:-220px;
  left:35%;
}

/* PARTICLES */

.particles{
  position:fixed;
  inset:0;
  overflow:hidden;
  pointer-events:none;
  z-index:1;
}

.particle{
  position:absolute;
  bottom:-10px;
  width:3px;
  height:3px;
  border-radius:50%;
  background:var(--cyan);
  box-shadow:0 0 12px var(--cyan);
  animation:float linear infinite;
}

.particle:nth-child(1){
  left:8%;
  animation-duration:7s;
}

.particle:nth-child(2){
  left:22%;
  background:var(--purple);
  box-shadow:0 0 12px var(--purple);
  animation-duration:9s;
  animation-delay:-4s;
}

.particle:nth-child(3){
  left:40%;
  animation-duration:6s;
  animation-delay:-2s;
}

.particle:nth-child(4){
  left:58%;
  background:var(--pink);
  box-shadow:0 0 12px var(--pink);
  animation-duration:8s;
  animation-delay:-5s;
}

.particle:nth-child(5){
  left:76%;
  background:var(--green);
  box-shadow:0 0 12px var(--green);
  animation-duration:10s;
  animation-delay:-7s;
}

.particle:nth-child(6){
  left:92%;
  animation-duration:7s;
  animation-delay:-3s;
}

@keyframes float{
  from{
    transform:translateY(10vh);
    opacity:0;
  }

  15%{
    opacity:1;
  }

  85%{
    opacity:1;
  }

  to{
    transform:translateY(-115vh);
    opacity:0;
  }
}

/* CONTAINER */

.container{
  position:relative;
  z-index:2;
  width:min(900px,92%);
  margin:auto;
  padding:30px 0 45px;
}

/* STATUS */

.status{
  display:flex;
  justify-content:center;
  align-items:center;
  gap:8px;
  margin-bottom:22px;
  color:#a7faff;
  font-size:10px;
  letter-spacing:4px;
}

.status-dot{
  width:7px;
  height:7px;
  border-radius:50%;
  background:var(--green);
  box-shadow:0 0 15px var(--green);
  animation:blink 1.2s infinite alternate;
}

@keyframes blink{
  from{opacity:.3}
  to{opacity:1}
}

/* HERO */

.hero{
  text-align:center;
  padding:25px 10px 35px;
}

/* BADGE */

.badge{
  display:inline-block;
  padding:8px 15px;
  border:1px solid rgba(0,234,255,.35);
  border-radius:999px;
  background:rgba(0,234,255,.05);
  color:#a5f8ff;
  font-size:10px;
  letter-spacing:3px;
  box-shadow:0 0 25px rgba(0,234,255,.08);
}

/* LOGO + NAME */

.brand{
  display:flex;
  align-items:center;
  justify-content:center;
  gap:22px;
  margin:28px auto 20px;
}

/* รูปโลโก้ของคุณถูกฝังอยู่ตรง src ด้านล่าง */

.brand-logo{
  display:block;
  width:145px;
  height:145px;
  object-fit:contain;

  filter:
    drop-shadow(0 0 12px rgba(0,234,255,.22))
    drop-shadow(0 0 28px rgba(168,85,255,.12));

  transition:.35s ease;
}

.brand-logo:hover{
  transform:scale(1.045);

  filter:
    drop-shadow(0 0 18px rgba(0,234,255,.45))
    drop-shadow(0 0 35px rgba(168,85,255,.25));
}

/* PACKCULT SHOP */

.brand-text{
  font-family:"Orbitron",sans-serif;
  font-size:clamp(24px,5vw,48px);
  font-weight:900;
  letter-spacing:3px;
  white-space:nowrap;
  color:#fff;

  text-shadow:
    0 0 8px var(--cyan),
    0 0 24px rgba(0,234,255,.55);

  animation:textGlow 3s ease-in-out infinite alternate;
}

@keyframes textGlow{

  from{
    text-shadow:
      0 0 5px var(--cyan),
      0 0 15px rgba(0,234,255,.25);
  }

  to{
    text-shadow:
      0 0 10px var(--cyan),
      0 0 30px rgba(0,234,255,.65),
      0 0 50px rgba(168,85,255,.2);
  }

}

/* SUBTITLE */

.subtitle{
  color:var(--muted);
  font-size:12px;
  letter-spacing:3px;
}

/* QUOTE */

.quote{
  margin:24px auto 0;
  max-width:650px;
  font-family:"Orbitron",sans-serif;
  font-size:clamp(14px,3vw,20px);
  line-height:1.6;
}

.quote span{
  color:var(--cyan);
  text-shadow:0 0 15px rgba(0,234,255,.7);
}

/* LINKS */

.links{
  display:grid;
  gap:15px;
  width:min(650px,100%);
  margin:auto;
}

.social-card{
  position:relative;

  display:flex;
  align-items:center;

  gap:16px;

  padding:18px 20px;

  color:#fff;
  text-decoration:none;

  border:1px solid rgba(255,255,255,.12);
  border-radius:20px;

  background:
    linear-gradient(
      135deg,
      rgba(255,255,255,.08),
      rgba(255,255,255,.025)
    );

  backdrop-filter:blur(15px);
  -webkit-backdrop-filter:blur(15px);

  overflow:hidden;

  transition:.3s ease;
}

.social-card:before{
  content:"";
  position:absolute;
  left:-120%;
  top:0;

  width:120%;
  height:2px;

  background:
    linear-gradient(
      90deg,
      transparent,
      var(--cyan),
      var(--purple),
      transparent
    );

  transition:.5s ease;
}

.social-card:hover:before{
  left:100%;
}

.social-card:hover{
  transform:translateY(-5px);

  border-color:rgba(0,234,255,.5);

  box-shadow:
    0 0 30px rgba(0,234,255,.13);
}

.instagram:hover{
  border-color:rgba(255,54,209,.5);

  box-shadow:
    0 0 30px rgba(255,54,209,.13);
}

/* ICON */

.icon{
  display:grid;
  place-items:center;

  width:52px;
  height:52px;

  flex-shrink:0;

  border-radius:16px;

  font:700 25px Arial;

  color:var(--cyan);

  background:rgba(0,234,255,.08);

  border:1px solid rgba(0,234,255,.25);
}

.instagram .icon{
  color:#ff55d8;
  background:rgba(255,54,209,.08);
  border-color:rgba(255,54,209,.3);
}

/* SOCIAL TEXT */

.social-info{
  flex:1;
}

.social-info strong{
  display:block;

  font-family:"Orbitron",sans-serif;

  font-size:14px;

  letter-spacing:1px;
}

.social-info small{
  display:block;

  margin-top:4px;

  color:#8d94a8;

  font-size:11px;
}

/* ARROW */

.arrow{
  color:var(--cyan);
  font-size:23px;
  transition:.3s;
}

.instagram .arrow{
  color:#ff55d8;
}

.social-card:hover .arrow{
  transform:translate(4px,-4px);
}

/* TIKTOK */

.coming-soon{
  position:relative;

  width:min(650px,100%);

  margin:42px auto 0;

  padding:30px 20px;

  text-align:center;

  overflow:hidden;

  border-radius:24px;

  border:1px solid rgba(168,85,255,.35);

  background:
    linear-gradient(
      135deg,
      rgba(168,85,255,.13),
      rgba(0,234,255,.045)
    );

  box-shadow:
    0 0 45px rgba(168,85,255,.08);
}

.coming-soon h2{
  font-family:"Orbitron",sans-serif;
  font-size:23px;
  letter-spacing:4px;

  text-shadow:
    0 0 20px rgba(168,85,255,.5);
}

.coming-soon p{
  margin-top:9px;
  color:#aeb5c7;
  font-size:13px;
}

.soon-badge{
  display:inline-block;

  margin-top:15px;

  padding:7px 13px;

  border-radius:999px;

  border:1px solid rgba(168,85,255,.45);

  color:#d7b8ff;

  font-size:9px;

  letter-spacing:3px;

  animation:
    soonGlow 2s infinite alternate;
}

@keyframes soonGlow{

  from{
    box-shadow:
      0 0 5px rgba(168,85,255,.1);
  }

  to{
    box-shadow:
      0 0 20px rgba(168,85,255,.35);
  }

}

/* FOOTER */

footer{
  margin-top:35px;

  text-align:center;

  color:#60677a;

  font-size:9px;

  letter-spacing:3px;
}

/* MOBILE */

@media(max-width:600px){

  .container{
    width:92%;
    padding-top:20px;
  }

  .hero{
    padding-top:22px;
  }

  .brand{
    gap:12px;
    margin-top:23px;
  }

  .brand-logo{
    width:92px;
    height:92px;
  }

  .brand-text{
    font-size:21px;
    letter-spacing:1.5px;
  }

  .subtitle{
    font-size:9px;
    letter-spacing:2px;
  }

  .social-card{
    padding:15px;
    border-radius:17px;
  }

  .icon{
    width:47px;
    height:47px;
    border-radius:14px;
  }

  .social-info strong{
    font-size:12px;
  }

  .social-info small{
    font-size:10px;
  }

  .arrow{
    font-size:20px;
  }

  .coming-soon{
    margin-top:35px;
  }

}

/* SMALL MOBILE */

@media(max-width:380px){

  .brand{
    gap:8px;
  }

  .brand-logo{
    width:75px;
    height:75px;
  }

  .brand-text{
    font-size:17px;
    letter-spacing:1px;
  }

  .badge{
    font-size:8px;
    letter-spacing:2px;
  }

}

/* REDUCE MOTION */

@media(prefers-reduced-motion:reduce){

  *,
  *::before,
  *::after{

    animation-duration:.01ms!important;
    animation-iteration-count:1!important;
    transition-duration:.01ms!important;
    scroll-behavior:auto!important;

  }

}
</style>
</head>

<body>

<div class="glow one"></div>
<div class="glow two"></div>
<div class="glow three"></div>

<div class="particles">
  <span class="particle"></span>
  <span class="particle"></span>
  <span class="particle"></span>
  <span class="particle"></span>
  <span class="particle"></span>
  <span class="particle"></span>
</div>

<main class="container">

  <div class="status">
    <span class="status-dot"></span>
    PACKCULT ONLINE
  </div>

  <section class="hero">

    <div class="badge">
      STREETWEAR • CULTURE • ATTITUDE
    </div>

    <div class="brand">

      <img
        class="brand-logo"
        alt="PACKCULT Logo"
        src="data:image/webp;base64,REPLACE_WITH_EMBEDDED_LOGO_DATA"
      >

      <div class="brand-text">
        PACKCULT SHOP
      </div>

    </div>

    <p class="subtitle">
      WEAR YOUR ATTITUDE. BUILD YOUR CULTURE.
    </p>

    <p class="quote">
      “<span>Wear what you believe.</span><br>
      Make your own culture.”
    </p>

  </section>

  <section class="links">

    <a
      class="social-card"
      href="https://www.facebook.com/share/18ZmcmhnFq/"
      target="_blank"
      rel="noopener noreferrer"
    >

      <div class="icon">f</div>

      <div class="social-info">
        <strong>FACEBOOK</strong>
        <small>ติดตาม PACKCULT SHOP</small>
      </div>

      <div class="arrow">↗</div>

    </a>

    <a
      class="social-card instagram"
      href="https://www.instagram.com/packcult.shop?igsh=ZDZybXI4cXV6ZGNs"
      target="_blank"
      rel="noopener noreferrer"
    >

      <div class="icon">◎</div>

      <div class="social-info">
        <strong>INSTAGRAM</strong>
        <small>@packcult.shop</small>
      </div>

      <div class="arrow">↗</div>

    </a>

  </section>

  <section class="coming-soon">

    <h2>TIKTOK</h2>

    <p>
      เร็วๆ นี้ พร้อมคอนเทนต์อีกมากมาย
    </p>

    <span class="soon-badge">
      COMING SOON
    </span>

  </section>

  <footer>
    © 2026 PACKCULT SHOP • ALL RIGHTS RESERVED
  </footer>

</main>

</body>
</html>

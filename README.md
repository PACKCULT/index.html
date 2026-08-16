<!DOCTYPE html>
<html lang="th">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>PACKCULT</title>

<style>

*{
  box-sizing:border-box;
  margin:0;
  padding:0;
}

html{
  scroll-behavior:smooth;
}

body{
  min-height:100vh;
  font-family:Arial,Helvetica,sans-serif;
  color:#111;
  overflow-x:hidden;

  background:
    radial-gradient(circle at 15% 10%, #ffffff 0%, transparent 28%),
    radial-gradient(circle at 85% 15%, #bcecff 0%, transparent 30%),
    linear-gradient(135deg,#f8f8f8,#d8d8d8,#ffffff);
}

/* =========================
   MOVING BLUE LIGHT
========================= */

body::before{
  content:"";
  position:fixed;

  width:420px;
  height:420px;

  top:-120px;
  left:-160px;

  border-radius:50%;

  background:rgba(0,174,255,.32);

  filter:blur(90px);

  animation:
    lightMove 9s ease-in-out infinite alternate;

  pointer-events:none;
}

body::after{
  content:"";
  position:fixed;

  width:330px;
  height:330px;

  right:-150px;
  bottom:-100px;

  border-radius:50%;

  background:rgba(0,110,255,.25);

  filter:blur(80px);

  animation:
    lightMove2 8s ease-in-out infinite alternate;

  pointer-events:none;
}

@keyframes lightMove{

  0%{
    transform:translate(0,0);
  }

  100%{
    transform:translate(620px,420px);
  }

}

@keyframes lightMove2{

  0%{
    transform:translate(0,0);
  }

  100%{
    transform:translate(-300px,-250px);
  }

}

/* =========================
   CONTAINER
========================= */

.container{
  width:100%;
  max-width:500px;

  margin:auto;

  padding:35px 18px 45px;

  position:relative;
  z-index:2;
}

/* =========================
   MAIN CARD
========================= */

.card{

  padding:35px 20px;

  border-radius:32px;

  background:
    linear-gradient(
      145deg,
      rgba(255,255,255,.78),
      rgba(255,255,255,.48)
    );

  border:1px solid rgba(255,255,255,.95);

  backdrop-filter:blur(22px);

  box-shadow:

    0 30px 80px rgba(0,0,0,.18),

    0 0 50px rgba(0,170,255,.12);

  animation:
    cardIn 1s ease;

}

@keyframes cardIn{

  from{
    opacity:0;
    transform:translateY(35px) scale(.97);
  }

  to{
    opacity:1;
    transform:translateY(0) scale(1);
  }

}

/* =========================
   PACKCULT LOGO
========================= */

.logo-area{

  position:relative;

  text-align:center;

  margin:10px 0 32px;

  overflow:hidden;

  padding:10px 0 20px;

}

.logo-text{

  position:relative;

  display:inline-block;

  font-size:45px;

  font-weight:1000;

  letter-spacing:6px;

  line-height:1;

  color:#111;

  text-transform:uppercase;

  text-shadow:

    0 2px 0 #fff,

    0 5px 15px rgba(0,0,0,.15);

  animation:
    logoAppear 1s ease;

}

.logo-text span{

  color:#007cff;

  text-shadow:

    0 0 10px rgba(0,124,255,.35),

    0 0 25px rgba(0,170,255,.18);

}

.logo-text::after{

  content:"";

  position:absolute;

  left:-20px;
  right:-20px;

  bottom:-12px;

  height:3px;

  border-radius:20px;

  background:

    linear-gradient(
      90deg,
      transparent,
      #00c8ff,
      #006eff,
      #00c8ff,
      transparent
    );

  box-shadow:

    0 0 12px #00aaff,

    0 0 25px rgba(0,170,255,.5);

  animation:
    blueLine 2.5s ease-in-out infinite;

}

@keyframes logoAppear{

  from{
    opacity:0;
    transform:scale(.75);
    letter-spacing:15px;
  }

  to{
    opacity:1;
    transform:scale(1);
    letter-spacing:6px;
  }

}

@keyframes blueLine{

  0%,100%{
    transform:scaleX(.65);
    opacity:.5;
  }

  50%{
    transform:scaleX(1);
    opacity:1;
  }

}

/* =========================
   OFFICIAL TAG
========================= */

.tag{

  display:inline-block;

  padding:7px 15px;

  margin-bottom:13px;

  border-radius:50px;

  background:#111;

  color:#fff;

  font-size:9px;

  font-weight:bold;

  letter-spacing:3px;

  box-shadow:

    0 0 15px rgba(0,170,255,.3);

  animation:
    tagPulse 2.5s infinite;

}

@keyframes tagPulse{

  0%,100%{
    box-shadow:
      0 0 8px rgba(0,170,255,.15);
  }

  50%{
    box-shadow:
      0 0 25px rgba(0,170,255,.45);
  }

}

/* =========================
   BRAND TEXT
========================= */

.brand{

  font-size:18px;

  font-weight:900;

  letter-spacing:4px;

  color:#333;

}

.tagline{

  margin-top:8px;

  margin-bottom:32px;

  color:#777;

  font-size:12px;

  letter-spacing:3px;

}

/* =========================
   SOCIAL BUTTON
========================= */

.social{

  position:relative;

  display:flex;

  align-items:center;

  width:100%;

  min-height:82px;

  margin:18px 0;

  padding:12px 18px;

  border-radius:22px;

  background:

    linear-gradient(
      135deg,
      rgba(255,255,255,.9),
      rgba(245,245,245,.65)
    );

  border:2px solid rgba(0,160,255,.28);

  color:#111;

  text-decoration:none;

  overflow:hidden;

  box-shadow:

    0 12px 30px rgba(0,0,0,.12),

    0 0 20px rgba(0,170,255,.08);

  transition:

    transform .3s ease,

    border-color .3s ease,

    box-shadow .3s ease;

}

/* BLUE EDGE */

.social::before{

  content:"";

  position:absolute;

  left:0;
  top:0;

  width:5px;
  height:100%;

  background:

    linear-gradient(
      #00c8ff,
      #006eff
    );

  box-shadow:

    0 0 18px #00aaff;

}

/* LIGHT SWEEP */

.social::after{

  content:"";

  position:absolute;

  width:100px;
  height:220%;

  top:-60px;
  left:-160px;

  background:

    linear-gradient(
      90deg,
      transparent,
      rgba(255,255,255,.7),
      transparent
    );

  transform:rotate(20deg);

  transition:.7s;

}

.social:hover::after{

  left:120%;

}

.social:hover{

  transform:
    translateY(-6px)
    scale(1.01);

  border-color:#00aaff;

  box-shadow:

    0 20px 40px rgba(0,0,0,.18),

    0 0 30px rgba(0,170,255,.3);

}

.social:active{

  transform:scale(.96);

}

/* =========================
   SOCIAL ICON
========================= */

.icon{

  width:52px;
  height:52px;

  border-radius:16px;

  background:#111;

  color:#fff;

  display:flex;

  align-items:center;

  justify-content:center;

  flex-shrink:0;

  position:relative;
  z-index:2;

  box-shadow:

    0 7px 18px rgba(0,0,0,.22),

    0 0 15px rgba(0,170,255,.15);

  transition:

    transform .3s ease,

    background .3s ease;

}

.social:hover .icon{

  transform:
    rotate(-5deg)
    scale(1.08);

  background:#007cff;

  box-shadow:

    0 0 22px rgba(0,124,255,.45);

}

.icon svg{

  width:28px;
  height:28px;

}

/* =========================
   SOCIAL TEXT
========================= */

.social-text{

  margin-left:15px;

  text-align:left;

  position:relative;
  z-index:2;

}

.social-title{

  font-size:16px;

  font-weight:900;

  letter-spacing:1px;

}

.social-sub{

  margin-top:4px;

  font-size:11px;

  color:#777;

}

/* =========================
   ARROW
========================= */

.arrow{

  margin-left:auto;

  color:#888;

  font-size:26px;

  position:relative;
  z-index:2;

  transition:.3s;

}

.social:hover .arrow{

  color:#007cff;

  transform:
    translateX(6px);

}

/* =========================
   QUOTE
========================= */

.quote{

  margin-top:30px;

  padding:22px 15px;

  border-radius:22px;

  background:

    linear-gradient(
      135deg,
      rgba(255,255,255,.7),
      rgba(190,235,255,.55)
    );

  border:

    1px solid
    rgba(0,170,255,.22);

  box-shadow:

    0 10px 25px rgba(0,0,0,.08);

}

.quote-main{

  font-size:18px;

  font-weight:1000;

  letter-spacing:1px;

}

.quote-sub{

  margin-top:8px;

  font-size:10px;

  color:#666;

  letter-spacing:3px;

}

/* =========================
   FOOTER
========================= */

.footer{

  margin-top:30px;

  padding-top:20px;

  border-top:
    1px solid
    rgba(0,0,0,.1);

  color:#777;

  font-size:10px;

  letter-spacing:3px;

}

/* =========================
   MOBILE
========================= */

@media(max-width:480px){

  .container{

    padding:
      22px
      14px
      35px;

  }

  .card{

    padding:
      30px
      15px;

    border-radius:27px;

  }

  .logo-text{

    font-size:34px;

    letter-spacing:4px;

  }

  .brand{

    font-size:16px;

  }

  .social{

    min-height:76px;

  }

}

</style>

</head>


<body>

<div class="container">

<div class="card">


  <!-- PACKCULT COVER -->

  <div class="logo-area">

    <div class="logo-text">
      PACK<span>CULT</span>
    </div>

  </div>


  <!-- OFFICIAL -->

  <div class="tag">
    OFFICIAL
  </div>


  <div class="brand">
    STREETWEAR • LIFESTYLE
  </div>


  <div class="tagline">
    เท่ได้ • BE YOUR STYLE
  </div>


  <!-- FACEBOOK -->

  <a
    class="social"
    href="https://www.facebook.com/share/1DVBxNLHAD/"
    target="_blank"
    rel="noopener noreferrer"
  >

    <div class="icon">

      <svg
        viewBox="0 0 24 24"
        fill="currentColor"
      >

        <path
          d="M14 8h3V4h-3c-3.3 0-5 2-5 5v3H6v4h3v8h4v-8h3l1-4h-4V9c0-.7.3-1 1-1z"
        />

      </svg>

    </div>


    <div class="social-text">

      <div class="social-title">
        FACEBOOK
      </div>

      <div class="social-sub">
        Follow PACKCULT
      </div>

    </div>


    <div class="arrow">
      →
    </div>

  </a>


  <!-- INSTAGRAM -->

  <a
    class="social"
    href="https://www.instagram.com/packcult.shop?igsh=ZDZybXI2cXV6ZGNs"
    target="_blank"
    rel="noopener noreferrer"
  >

    <div class="icon">

      <svg
        viewBox="0 0 24 24"
        fill="none"
        stroke="currentColor"
        stroke-width="2"
      >

        <rect
          x="3"
          y="3"
          width="18"
          height="18"
          rx="5"
        />

        <circle
          cx="12"
          cy="12"
          r="4"
        />

        <circle
          cx="17.5"
          cy="6.5"
          r="1"
          fill="currentColor"
          stroke="none"
        />

      </svg>

    </div>


    <div class="social-text">

      <div class="social-title">
        INSTAGRAM
      </div>

      <div class="social-sub">
        @packcult.shop
      </div>

    </div>


    <div class="arrow">
      →
    </div>

  </a>


  <!-- QUOTE -->

  <div class="quote">

    <div class="quote-main">
      WEAR YOUR ATTITUDE.
    </div>

    <div class="quote-sub">
      PACKCULT
    </div>

  </div>


  <!-- FOOTER -->

  <div class="footer">
    PACKCULT © 2026
  </div>


</div>

</div>

</body>
</html>

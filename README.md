<!DOCTYPE html>
<html lang="th">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>PACK CULT</title>

<style>
*{
  box-sizing:border-box;
  margin:0;
  padding:0;
}

body{
  min-height:100vh;
  font-family:Arial,Helvetica,sans-serif;
  color:#111;
  overflow-x:hidden;

  background:
    radial-gradient(circle at 15% 10%, #ffffff 0%, transparent 30%),
    radial-gradient(circle at 85% 20%, #b9ecff 0%, transparent 28%),
    linear-gradient(135deg,#f5f5f5,#d7d7d7,#ffffff);
}

/* BLUE LIGHT */

body::before{
  content:"";
  position:fixed;

  width:420px;
  height:420px;

  top:-120px;
  left:-160px;

  border-radius:50%;

  background:rgba(0,170,255,.35);
  filter:blur(90px);

  animation:blueMove 9s ease-in-out infinite alternate;

  pointer-events:none;
}

@keyframes blueMove{
  0%{
    transform:translate(0,0);
  }

  100%{
    transform:translate(650px,400px);
  }
}

/* SECOND LIGHT */

body::after{
  content:"";
  position:fixed;

  width:300px;
  height:300px;

  right:-120px;
  bottom:-80px;

  border-radius:50%;

  background:rgba(0,110,255,.25);
  filter:blur(80px);

  animation:blueMove2 7s ease-in-out infinite alternate;

  pointer-events:none;
}

@keyframes blueMove2{
  0%{
    transform:translate(0,0);
  }

  100%{
    transform:translate(-250px,-200px);
  }
}

/* MAIN */

.container{
  width:100%;
  max-width:500px;
  margin:auto;

  padding:40px 18px;

  text-align:center;

  position:relative;
  z-index:2;
}

/* CARD */

.card{
  padding:32px 20px;

  border-radius:30px;

  background:rgba(255,255,255,.62);

  border:1px solid rgba(255,255,255,.9);

  backdrop-filter:blur(20px);

  box-shadow:
    0 25px 70px rgba(0,0,0,.18),
    0 0 45px rgba(0,160,255,.10);

  animation:cardIn 1s ease;
}

@keyframes cardIn{
  from{
    opacity:0;
    transform:translateY(35px);
  }

  to{
    opacity:1;
    transform:translateY(0);
  }
}

/* LOGO */

.logo-wrap{
  position:relative;

  width:140px;
  height:140px;

  margin:0 auto 18px;

  display:flex;
  align-items:center;
  justify-content:center;
}

.logo-wrap::before{
  content:"";

  position:absolute;

  width:140px;
  height:140px;

  border-radius:50%;

  border:3px solid transparent;

  border-top-color:#00aaff;
  border-right-color:#006eff;

  box-shadow:
    0 0 20px rgba(0,170,255,.45);

  animation:spin 4s linear infinite;
}

.logo-wrap::after{
  content:"";

  position:absolute;

  width:120px;
  height:120px;

  border-radius:50%;

  border:1px solid rgba(0,170,255,.3);

  animation:pulseRing 2s ease-in-out infinite;
}

@keyframes spin{
  to{
    transform:rotate(360deg);
  }
}

@keyframes pulseRing{
  0%,100%{
    transform:scale(.95);
    opacity:.5;
  }

  50%{
    transform:scale(1.05);
    opacity:1;
  }
}

.logo{
  width:105px;
  height:105px;

  border-radius:50%;

  background:#111;
  color:#fff;

  display:flex;
  align-items:center;
  justify-content:center;

  font-size:32px;
  font-weight:900;

  letter-spacing:-3px;

  box-shadow:
    0 12px 35px rgba(0,0,0,.3),
    0 0 25px rgba(0,170,255,.25);

  position:relative;
  z-index:2;
}

/* OFFICIAL */

.tag{
  display:inline-block;

  padding:7px 15px;

  margin-bottom:12px;

  border-radius:50px;

  background:#111;

  color:#fff;

  font-size:10px;

  letter-spacing:3px;

  box-shadow:
    0 0 15px rgba(0,170,255,.25);
}

/* BRAND */

.brand{
  font-size:39px;

  font-weight:1000;

  letter-spacing:7px;

  color:#111;

  animation:brandIn 1s ease;
}

@keyframes brandIn{
  from{
    opacity:0;
    letter-spacing:15px;
  }

  to{
    opacity:1;
    letter-spacing:7px;
  }
}

.tagline{
  margin-top:9px;
  margin-bottom:30px;

  color:#555;

  font-size:13px;

  letter-spacing:3px;
}

/* SOCIAL CARDS */

.social{
  position:relative;

  display:flex;
  align-items:center;

  width:100%;

  min-height:78px;

  margin:18px 0;

  padding:12px 18px;

  border-radius:20px;

  text-decoration:none;

  color:#111;

  background:rgba(255,255,255,.8);

  border:2px solid rgba(0,170,255,.35);

  box-shadow:
    0 10px 30px rgba(0,0,0,.12),
    0 0 20px rgba(0,170,255,.08);

  overflow:hidden;

  transition:
    transform .3s ease,
    border-color .3s ease,
    box-shadow .3s ease;
}

/* BLUE LINE */

.social::before{
  content:"";

  position:absolute;

  left:0;
  top:0;

  width:5px;
  height:100%;

  background:linear-gradient(
    #00c8ff,
    #006eff
  );

  box-shadow:
    0 0 18px #00aaff;
}

/* SHINE */

.social::after{
  content:"";

  position:absolute;

  width:100px;
  height:200%;

  top:-50%;
  left:-150px;

  background:rgba(255,255,255,.6);

  transform:rotate(20deg);

  transition:.7s;
}

.social:hover::after{
  left:120%;
}

.social:hover{
  transform:translateY(-5px);

  border-color:#00aaff;

  box-shadow:
    0 18px 40px rgba(0,0,0,.2),
    0 0 25px rgba(0,170,255,.3);
}

.social:active{
  transform:scale(.97);
}

/* ICON */

.icon{
  width:50px;
  height:50px;

  border-radius:15px;

  display:flex;
  align-items:center;
  justify-content:center;

  flex-shrink:0;

  background:#111;

  color:#fff;

  box-shadow:
    0 5px 15px rgba(0,0,0,.2);

  position:relative;
  z-index:2;
}

.icon svg{
  width:27px;
  height:27px;
}

/* TEXT */

.social-text{
  text-align:left;

  margin-left:15px;

  position:relative;
  z-index:2;
}

.social-title{
  font-size:16px;

  font-weight:900;

  letter-spacing:1px;
}

.social-sub{
  margin-top:3px;

  font-size:11px;

  color:#777;
}

/* ARROW */

.arrow{
  margin-left:auto;

  font-size:25px;

  color:#888;

  position:relative;
  z-index:2;

  transition:.3s;
}

.social:hover .arrow{
  color:#00aaff;
  transform:translateX(5px);
}

/* QUOTE */

.quote{
  margin-top:28px;

  padding:20px;

  border-radius:20px;

  background:linear-gradient(
    135deg,
    rgba(255,255,255,.7),
    rgba(190,235,255,.5)
  );

  border:1px solid rgba(0,170,255,.2);
}

.quote-main{
  font-size:18px;
  font-weight:900;
  letter-spacing:1px;
}

.quote-sub{
  margin-top:7px;

  font-size:11px;

  color:#666;

  letter-spacing:2px;
}

/* FOOTER */

.footer{
  margin-top:30px;

  padding-top:20px;

  border-top:1px solid rgba(0,0,0,.1);

  font-size:10px;

  color:#777;

  letter-spacing:3px;
}

/* MOBILE */

@media(max-width:480px){

  .container{
    padding-top:25px;
  }

  .card{
    padding:28px 16px;
    border-radius:26px;
  }

  .brand{
    font-size:30px;
    letter-spacing:5px;
  }

  .social{
    min-height:74px;
  }
}
</style>

</head>

<body>

<div class="container">

<div class="card">

  <!-- LOGO -->

  <div class="logo-wrap">

    <div class="logo">
      PC
    </div>

  </div>


  <div class="tag">
    OFFICIAL
  </div>


  <div class="brand">
    PACK CULT
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
        <path d="M14 8h3V4h-3c-3.3 0-5 2-5 5v3H6v4h3v8h4v-8h3l1-4h-4V9c0-.7.3-1 1-1z"/>
      </svg>

    </div>

    <div class="social-text">

      <div class="social-title">
        FACEBOOK
      </div>

      <div class="social-sub">
        Follow PACK CULT
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
      PACK CULT
    </div>

  </div>


  <div class="footer">
    PACK CULT © 2026
  </div>

</div>

</div>

</body>
</html>

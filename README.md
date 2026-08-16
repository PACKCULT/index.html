<!DOCTYPE html>
<html lang="th">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>PACK CULT — BE YOUR STYLE</title>

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
  background:#050505;
  color:#fff;
  font-family:Arial,Helvetica,sans-serif;
  overflow-x:hidden;
}

/* Background */

body::before{
  content:"";
  position:fixed;
  width:500px;
  height:500px;
  top:-250px;
  left:50%;
  transform:translateX(-50%);
  background:#333;
  filter:blur(150px);
  opacity:.25;
  pointer-events:none;
}

/* Main */

.container{
  width:100%;
  max-width:500px;
  margin:auto;
  padding:55px 22px 35px;
  text-align:center;
}

/* Logo */

.logo{
  width:125px;
  height:125px;
  margin:0 auto 25px;

  border:2px solid #fff;
  border-radius:50%;

  display:flex;
  align-items:center;
  justify-content:center;

  background:#080808;

  font-size:34px;
  font-weight:900;
  letter-spacing:-3px;

  box-shadow:
    0 0 0 7px #111,
    0 0 40px rgba(255,255,255,.12);

  animation:logoIn 1s ease;
}

@keyframes logoIn{
  from{
    opacity:0;
    transform:scale(.7) rotate(-10deg);
  }
  to{
    opacity:1;
    transform:scale(1) rotate(0);
  }
}

/* Brand */

.brand{
  font-size:38px;
  font-weight:900;
  letter-spacing:7px;
  margin-bottom:12px;

  animation:fadeUp .8s ease;
}

.tagline{
  color:#888;
  font-size:13px;
  letter-spacing:3px;
  margin-bottom:38px;

  animation:fadeUp 1s ease;
}

@keyframes fadeUp{
  from{
    opacity:0;
    transform:translateY(15px);
  }
  to{
    opacity:1;
    transform:translateY(0);
  }
}

/* Buttons */

.button{
  position:relative;

  display:flex;
  align-items:center;
  justify-content:center;

  width:100%;
  height:65px;

  margin:16px 0;

  color:#fff;
  text-decoration:none;

  border:1px solid #292929;
  border-radius:18px;

  background:
    linear-gradient(
      135deg,
      #1d1d1d,
      #090909
    );

  font-size:15px;
  font-weight:800;
  letter-spacing:2px;

  overflow:hidden;

  box-shadow:
    0 10px 30px rgba(0,0,0,.5);

  transition:
    transform .25s ease,
    border-color .25s ease,
    box-shadow .25s ease;
}

.button::before{
  content:"";
  position:absolute;
  top:0;
  left:-100%;
  width:100%;
  height:100%;

  background:
    linear-gradient(
      90deg,
      transparent,
      rgba(255,255,255,.12),
      transparent
    );

  transition:left .5s ease;
}

.button:hover::before{
  left:100%;
}

.button:hover{
  transform:translateY(-4px);
  border-color:#666;

  box-shadow:
    0 15px 40px rgba(0,0,0,.8);
}

.button:active{
  transform:scale(.97);
}

.arrow{
  position:absolute;
  right:22px;

  font-size:25px;
  color:#777;

  transition:
    transform .25s ease,
    color .25s ease;
}

.button:hover .arrow{
  transform:translateX(5px);
  color:#fff;
}

/* Featured */

.featured{
  margin:38px 0 25px;
  padding:20px;

  border:1px solid #222;
  border-radius:18px;

  background:#0b0b0b;
}

.featured-title{
  font-size:11px;
  color:#666;
  letter-spacing:3px;
  margin-bottom:8px;
}

.featured-text{
  font-size:18px;
  font-weight:800;
  letter-spacing:1px;
}

/* Footer */

.footer{
  margin-top:45px;
  padding-top:20px;

  border-top:1px solid #1b1b1b;

  color:#444;
  font-size:10px;
  letter-spacing:3px;
}

/* Mobile */

@media(max-width:480px){

  .container{
    padding-top:40px;
  }

  .brand{
    font-size:30px;
    letter-spacing:5px;
  }

  .logo{
    width:110px;
    height:110px;
    font-size:30px;
  }

  .button{
    height:62px;
  }
}
</style>
</head>

<body>

<div class="container">

  <div class="logo">
    PC
  </div>

  <div class="brand">
    PACK CULT
  </div>

  <div class="tagline">
    เท่ได้ • BE YOUR STYLE
  </div>


  <a
    class="button"
    href="https://www.facebook.com/share/1DVBxNLHAD/"
    target="_blank"
    rel="noopener noreferrer"
  >
    FACEBOOK
    <span class="arrow">›</span>
  </a>


  <a
    class="button"
    href="https://www.instagram.com/packcult.shop?igsh=ZDZybXI2cXV6ZGNs"
    target="_blank"
    rel="noopener noreferrer"
  >
    INSTAGRAM
    <span class="arrow">›</span>
  </a>


  <div class="featured">
    <div class="featured-title">
      PACK CULT
    </div>

    <div class="featured-text">
      WEAR YOUR ATTITUDE.
    </div>
  </div>


  <div class="footer">
    PACK CULT © 2026
  </div>

</div>

</body>
</html>

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
    radial-gradient(circle at 20% 10%, #ffffff 0%, transparent 30%),
    radial-gradient(circle at 80% 20%, #d9d9d9 0%, transparent 28%),
    linear-gradient(135deg,#eeeeee,#bcbcbc,#f7f7f7);
}

/* Moving light */

body::before{
  content:"";
  position:fixed;
  width:350px;
  height:350px;

  top:10%;
  left:-150px;

  border-radius:50%;

  background:rgba(255,255,255,.75);
  filter:blur(70px);

  animation:lightMove 8s ease-in-out infinite alternate;

  pointer-events:none;
}

@keyframes lightMove{
  0%{
    transform:translate(0,0);
  }

  100%{
    transform:translate(600px,250px);
  }
}

/* Container */

.container{
  width:100%;
  max-width:500px;
  margin:auto;

  padding:45px 20px 40px;

  text-align:center;

  position:relative;
  z-index:2;
}

/* Glass card */

.card{
  padding:35px 22px;

  border-radius:30px;

  background:rgba(255,255,255,.55);

  border:1px solid rgba(255,255,255,.8);

  backdrop-filter:blur(18px);

  box-shadow:
    0 25px 60px rgba(0,0,0,.18);

  animation:cardIn 1s ease;
}

@keyframes cardIn{
  from{
    opacity:0;
    transform:translateY(30px);
  }

  to{
    opacity:1;
    transform:translateY(0);
  }
}

/* Logo */

.logo-wrap{
  position:relative;

  width:135px;
  height:135px;

  margin:0 auto 25px;

  display:flex;
  align-items:center;
  justify-content:center;
}

/* spinning ring */

.logo-wrap::before{
  content:"";

  position:absolute;

  width:135px;
  height:135px;

  border-radius:50%;

  border:2px solid transparent;

  border-top-color:#111;
  border-right-color:#777;

  animation:spin 5s linear infinite;
}

@keyframes spin{
  to{
    transform:rotate(360deg);
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
    0 12px 30px rgba(0,0,0,.3);
}

/* Brand */

.brand{
  font-size:40px;
  font-weight:1000;

  letter-spacing:7px;

  color:#111;

  text-shadow:
    0 3px 0 rgba(255,255,255,.6);

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
  margin-top:10px;
  margin-bottom:32px;

  font-size:13px;

  letter-spacing:3px;

  color:#555;
}

/* Buttons */

.button{
  position:relative;

  display:flex;
  align-items:center;
  justify-content:center;

  height:65px;

  margin:15px 0;

  border-radius:18px;

  text-decoration:none;

  color:#fff;

  background:
    linear-gradient(
      135deg,
      #171717,
      #3b3b3b
    );

  border:1px solid rgba(0,0,0,.3);

  font-size:15px;
  font-weight:bold;

  letter-spacing:2px;

  overflow:hidden;

  box-shadow:
    0 12px 25px rgba(0,0,0,.2);

  transition:
    transform .25s,
    box-shadow .25s;
}

/* shine */

.button::before{
  content:"";

  position:absolute;

  width:80px;
  height:200%;

  top:-50%;
  left:-120px;

  background:rgba(255,255,255,.25);

  transform:rotate(20deg);

  transition:.6s;
}

.button:hover::before{
  left:120%;
}

.button:hover{
  transform:translateY(-5px) scale(1.01);

  box-shadow:
    0 18px 35px rgba(0,0,0,.3);
}

.button:active{
  transform:scale(.96);
}

.arrow{
  position:absolute;

  right:20px;

  font-size:24px;

  transition:.3s;
}

.button:hover .arrow{
  transform:translateX(6px);
}

/* Tag */

.tag{
  display:inline-block;

  margin:5px 0 25px;

  padding:7px 14px;

  border-radius:50px;

  background:#111;

  color:#fff;

  font-size:10px;

  letter-spacing:2px;

  animation:pulse 2s infinite;
}

@keyframes pulse{
  0%,100%{
    box-shadow:0 0 0 rgba(0,0,0,0);
  }

  50%{
    box-shadow:0 0 20px rgba(0,0,0,.25);
  }
}

/* Quote */

.quote{
  margin-top:30px;

  padding:18px;

  border-radius:18px;

  background:rgba(255,255,255,.45);

  border:1px solid rgba(255,255,255,.7);

  font-size:14px;

  font-weight:bold;

  letter-spacing:1px;
}

.quote span{
  display:block;

  margin-top:7px;

  font-size:11px;

  color:#777;

  font-weight:normal;
}

/* Footer */

.footer{
  margin-top:30px;

  font-size:10px;

  letter-spacing:3px;

  color:#777;
}

/* Mobile */

@media(max-width:480px){

  .container{
    padding-top:25px;
  }

  .card{
    padding:30px 18px;
    border-radius:25px;
  }

  .brand{
    font-size:30px;
    letter-spacing:5px;
  }

  .button{
    height:62px;
  }
}
</style>

</head>

<body>

<div class="container">

<div class="card">

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


  <a
    class="button"
    href="https://www.facebook.com/share/1DVBxNLHAD/"
    target="_blank"
    rel="noopener noreferrer"
  >
    FACEBOOK
    <span class="arrow">→</span>
  </a>


  <a
    class="button"
    href="https://www.instagram.com/packcult.shop?igsh=ZDZybXI2cXV6ZGNs"
    target="_blank"
    rel="noopener noreferrer"
  >
    INSTAGRAM
    <span class="arrow">→</span>
  </a>


  <div class="quote">
    WEAR YOUR ATTITUDE.
    <span>PACK CULT</span>
  </div>

  <div class="footer">
    PACK CULT © 2026
  </div>

</div>

</div>

</body>
</html>

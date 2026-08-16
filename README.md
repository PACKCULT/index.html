<!DOCTYPE html>
<html lang="th">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>PACKCULT SHOP</title>

<style>
*{
  box-sizing:border-box;
}

body{
  margin:0;
  min-height:100vh;
  font-family:Arial,"Noto Sans Thai",sans-serif;
  color:white;
  background:
    radial-gradient(circle at 20% 10%,#444 0%,transparent 30%),
    radial-gradient(circle at 90% 90%,#333 0%,transparent 35%),
    #050505;
  display:flex;
  justify-content:center;
  align-items:center;
  padding:20px;
  overflow-x:hidden;
}

body:before{
  content:"";
  position:fixed;
  width:250px;
  height:250px;
  border-radius:50%;
  background:#fff;
  opacity:.06;
  filter:blur(70px);
  top:-80px;
  left:-80px;
  animation:move 7s infinite alternate;
}

.card{
  width:100%;
  max-width:500px;
  padding:35px 22px 25px;
  text-align:center;
  background:linear-gradient(145deg,#242424,#090909);
  border:1px solid #ffffff25;
  border-radius:30px;
  box-shadow:
    0 25px 80px #000,
    inset 0 1px #ffffff18;
  animation:show .8s ease;
}

.logo{
  width:180px;
  height:180px;
  border-radius:50%;
  object-fit:cover;
  border:5px solid #111;
  box-shadow:
    0 0 0 2px #ffffff40,
    0 0 35px #ffffff22;
  margin-bottom:18px;
}

h1{
  margin:0;
  font-size:30px;
  font-weight:900;
  letter-spacing:3px;
}

.sub{
  margin-top:8px;
  margin-bottom:22px;
  color:#999;
  font-size:11px;
  letter-spacing:4px;
}

.message{
  color:#ddd;
  font-size:16px;
  line-height:1.9;
  margin-bottom:25px;
}

.fire{
  display:inline-block;
  animation:fire 1s infinite alternate;
}

.buttons{
  display:grid;
  gap:13px;
}

.btn{
  min-height:60px;
  display:flex;
  align-items:center;
  justify-content:center;
  border-radius:17px;
  text-decoration:none;
  font-size:16px;
  font-weight:900;
  transition:.25s;
}

.btn:hover{
  transform:translateY(-4px);
  box-shadow:0 12px 30px #000;
}

.facebook{
  background:white;
  color:#050505;
}

.instagram{
  background:#111;
  color:white;
  border:1px solid #ffffff55;
}

.icon{
  margin-right:10px;
  font-size:22px;
  font-weight:900;
}

.footer{
  margin-top:22px;
  color:#666;
  font-size:11px;
  letter-spacing:1px;
}

@keyframes show{
  from{
    opacity:0;
    transform:translateY(30px) scale(.96);
  }
  to{
    opacity:1;
    transform:none;
  }
}

@keyframes move{
  from{
    transform:translate(0,0);
  }
  to{
    transform:translate(120px,100px);
  }
}

@keyframes fire{
  from{
    transform:translateY(0) rotate(-3deg);
  }
  to{
    transform:translateY(-5px) rotate(3deg);
  }
}

@media(max-width:430px){
  .card{
    padding:28px 17px 22px;
  }

  .logo{
    width:155px;
    height:155px;
  }

  h1{
    font-size:25px;
  }

  .message{
    font-size:15px;
  }
}
</style>
</head>

<body>

<div class="card">

  <!-- โลโก้แบบตัวอักษร -->
  <div style="
    width:180px;
    height:180px;
    border-radius:50%;
    margin:0 auto 18px;
    display:flex;
    align-items:center;
    justify-content:center;
    background:#fff;
    color:#111;
    border:6px solid #111;
    box-shadow:0 0 0 2px #ffffff40,0 0 35px #ffffff22;
    font-size:22px;
    font-weight:900;
    letter-spacing:2px;
  ">
    PACKCULT
  </div>

  <h1>PACKCULT SHOP</h1>

  <div class="sub">
    OFFICIAL SOCIAL LINKS
  </div>

  <div class="message">
    ความฝันเล็กๆของเด็กสามคนที่อยากมีธุรกิจเป็นของตัวเอง
    <span class="fire">🔥</span>
    <br>
    ฝากติดตามแฟนเพจและสนับสนุนพวกเราด้วยนะครับ 🥰
  </div>

  <div class="buttons">

    <a
      class="btn facebook"
      href="https://www.facebook.com/share/1DVBxNLHAD/"
      target="_blank"
    >
      <span class="icon">f</span>
      ติดตามแฟนเพจ Facebook
    </a>

    <a
      class="btn instagram"
      href="https://www.instagram.com/packcult.shop?igsh=ZDZybXI2cXV6ZGNs"
      target="_blank"
    >
      <span class="icon">◎</span>
      ติดตาม Instagram
    </a>

  </div>

  <div class="footer">
    © PACKCULT SHOP • DREAM BIG • START SMALL ❤️
  </div>

</div>

</body>
</html>

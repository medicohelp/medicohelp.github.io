<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Medico Help</title>

<!-- Google Fonts -->
<link href="https://fonts.googleapis.com/css2?family=Poppins:wght@600;700&family=Inter:wght@400;500&display=swap" rel="stylesheet">

<style>
:root{
  --bg:#F9FBFD;
  --card:#ffffff;
  --text:#2b2b2b;
  --primary:#0B3C5D;
  --accent:#16A085;
}

body.dark{
  --bg:#0E1621;
  --card:#162235;
  --text:#E5E7EB;
  --primary:#60A5FA;
  --accent:#2ECC71;
}

*{box-sizing:border-box;transition:0.3s}

body{
  margin:0;
  font-family:'Inter',sans-serif;
  background:var(--bg);
  color:var(--text);
}

/* ================= NAVBAR ================= */
nav{
  position:sticky;
  top:0;
  z-index:1000;
  background:var(--card);
  display:flex;
  align-items:center;
  justify-content:space-between;
  padding:10px 6%;
  box-shadow:0 2px 10px rgba(0,0,0,0.08);
}

nav img{height:65px}

nav ul{
  list-style:none;
  display:flex;
  gap:20px;
}

nav a{
  text-decoration:none;
  font-weight:500;
  color:var(--text);
}

nav a:hover{color:var(--accent)}

.nav-right{
  display:flex;
  gap:10px;
}

.toggle, .login-btn{
  background:var(--accent);
  color:white;
  padding:6px 14px;
  border-radius:20px;
  cursor:pointer;
  font-size:14px;
}

/* ================= HERO ================= */
.hero{
  height:60vh;
  position:relative;
  overflow:hidden;
}

.slide{
  position:absolute;
  inset:0;
  background-size:cover;
  background-position:center;
  opacity:0;
}

.slide.active{opacity:1}

.hero-overlay{
  height:100%;
  background:rgba(0,0,0,0.55);
  display:flex;
  align-items:center;
  padding-left:8%;
}

.hero-text h1{
  font-family:'Poppins',sans-serif;
  font-size:44px;
  color:white;
}

.hero-text h2{
  font-size:20px;
  color:var(--accent);
  margin-top:-10px;
}

.hero-text p{
  max-width:520px;
  color:#ddd;
  font-size:16px;
}

/* ================= SEARCH ================= */
.search-box{
  margin-top:20px;
}

.search-box input{
  padding:12px;
  width:280px;
  border-radius:25px;
  border:none;
  outline:none;
}

/* ================= ABOUT ================= */
.about{
  padding:50px 8%;
  text-align:center;
}

.about h3{
  font-family:'Poppins',sans-serif;
  color:var(--primary);
  font-size:28px;
}

.about p{
  max-width:800px;
  margin:auto;
  font-size:16px;
}

/* ================= ICONS ================= */
.icons{
  display:flex;
  justify-content:center;
  gap:40px;
  margin-top:30px;
}

.icon{
  text-align:center;
  animation:float 2.5s ease-in-out infinite;
}

.icon span{
  font-size:40px;
}

@keyframes float{
  0%,100%{transform:translateY(0)}
  50%{transform:translateY(-8px)}
}

/* ================= FOOTER ================= */
footer{
  background:var(--primary);
  color:white;
  padding:15px;
  text-align:center;
  font-size:13px;
}

/* ================= POPUP ================= */
.popup{
  position:fixed;
  inset:0;
  background:rgba(0,0,0,0.6);
  display:flex;
  align-items:center;
  justify-content:center;
  z-index:2000;
}

.popup-content{
  background:white;
  padding:25px;
  max-width:420px;
  border-radius:12px;
  text-align:center;
}

.popup-content button{
  margin-top:15px;
  padding:8px 16px;
  border:none;
  background:var(--accent);
  color:white;
  border-radius:20px;
  cursor:pointer;
}

/* ================= LOGIN ================= */
.login-modal{
  display:none;
  position:fixed;
  inset:0;
  background:rgba(0,0,0,0.6);
  align-items:center;
  justify-content:center;
}

.login-box{
  background:white;
  padding:25px;
  border-radius:12px;
  width:300px;
}

.login-box input{
  width:100%;
  padding:10px;
  margin-bottom:12px;
}
</style>
</head>

<body>

<!-- POPUP -->
<div class="popup" id="popup">
  <div class="popup-content">
    <h3>Welcome to Medico Help</h3>
    <p>This website is created to support medicos across India.</p>
    <button onclick="closePopup()">Continue</button>
  </div>
</div>

<!-- LOGIN -->
<div class="login-modal" id="login">
  <div class="login-box">
    <h3>Login</h3>
    <input placeholder="Email">
    <input placeholder="Password" type="password">
    <button class="login-btn" onclick="closeLogin()">Login</button>
  </div>
</div>

<nav>
  <img src="logo.png">
  <ul>
    <li><a href="#">Home</a></li>
    <li><a href="#">Exams</a></li>
    <li><a href="#">Resources</a></li>
    <li><a href="#">Jobs</a></li>
  </ul>
  <div class="nav-right">
    <div class="toggle" onclick="toggleMode()">🌙</div>
    <div class="login-btn" onclick="openLogin()">Login</div>
  </div>
</nav>

<section class="hero">
  <div class="slide active" style="background-image:url('slide1.jpg')">
    <div class="hero-overlay">
      <div class="hero-text">
        <h1>Medico Help</h1>
        <h2>One for all and all for one</h2>
        <p>Helping every medico — from dream to degree and beyond.</p>

        <div class="search-box">
          <input placeholder="Search exams, jobs, notes...">
        </div>
      </div>
    </div>
  </div>
</section>

<section class="about">
  <h3>About Medico Help</h3>
  <p>
    Medico Help is dedicated to every student and doctor who dreams, studies,
    serves, and grows in the medical field. A trusted companion for guidance,
    resources, exams, and opportunities.
  </p>

  <div class="icons">
    <div class="icon"><span>📘</span><p>Exams</p></div>
    <div class="icon"><span>🩺</span><p>Practice</p></div>
    <div class="icon"><span>🏥</span><p>Jobs</p></div>
    <div class="icon"><span>📢</span><p>Notices</p></div>
  </div>
</section>

<footer>
  Disclaimer: This site is for information and helping purpose only.
</footer>

<script>
let slides=document.querySelectorAll(".slide"),i=0;
setInterval(()=>{
slides[i].classList.remove("active");
i=(i+1)%slides.length;
slides[i].classList.add("active");
},5000);

function toggleMode(){
document.body.classList.toggle("dark");
}

function closePopup(){
document.getElementById("popup").style.display="none";
}

function openLogin(){
document.getElementById("login").style.display="flex";
}

function closeLogin(){
document.getElementById("login").style.display="none";
}
</script>

</body>
</html>
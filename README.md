<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Medico Help | One for all, all for one</title>

<style>
body {
  margin: 0;
  font-family: Arial, sans-serif;
}

/* HEADER */
header {
  position: absolute;
  top: 0;
  width: 100%;
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 15px 20px;
  z-index: 10;
}

.logo-box {
  display: flex;
  align-items: center;
  gap: 10px;
}

.logo-box img {
  height: 45px;
}

.logo-box span {
  color: white;
  font-size: 20px;
  font-weight: bold;
}

/* HERO */
.hero {
  height: 100vh;
  background: 
    linear-gradient(rgba(0,0,0,0.6), rgba(0,0,0,0.6)),
    url("medical-bg.jpg") center/cover no-repeat;
  display: flex;
  align-items: center;
  padding-left: 8%;
  color: white;
}

.hero h1 {
  font-size: 48px;
  color: #7CFF6B;
}

.hero p {
  font-size: 20px;
  max-width: 600px;
}

/* SLIDING TEXT */
.slider-text {
  margin-top: 20px;
  font-size: 22px;
  color: #FFD166;
  animation: slide 6s infinite;
}

@keyframes slide {
  0% {opacity: 0;}
  20% {opacity: 1;}
  80% {opacity: 1;}
  100% {opacity: 0;}
}

/* SLIDER DOTS */
.dots {
  position: absolute;
  bottom: 30px;
  left: 8%;
}

.dots span {
  margin-right: 10px;
  font-size: 20px;
  opacity: 0.6;
}

.dots span.active {
  color: #7CFF6B;
  opacity: 1;
}

/* FOOTER */
footer {
  background: #1a1a1a;
  color: #ccc;
  text-align: center;
  padding: 15px;
  font-size: 14px;
}
</style>
</head>

<body>

<header>
  <div class="logo-box">
    <img src="logo.png" alt="Medico Help Logo">
    <span>Medico Help</span>
  </div>
</header>

<section class="hero">
  <div>
    <h1>Medico Help</h1>
    <p>One for all, all for one.</p>
    <div class="slider-text">
      Exams • Study Resources • AI in Medicine • Jobs & Notices
    </div>
  </div>

  <div class="dots">
    <span>1</span>
    <span class="active">2</span>
    <span>3</span>
    <span>4</span>
  </div>
</section>

<footer>
  Disclaimer: This site is just for information and helping purpose.
</footer>

</body>
</html>
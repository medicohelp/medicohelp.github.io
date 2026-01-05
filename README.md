<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Medico Help | One for all and all for one</title>

<!-- Google Fonts -->
<link href="https://fonts.googleapis.com/css2?family=Poppins:wght@600;700&family=Inter:wght@400;500&display=swap" rel="stylesheet">

<style>
* {
  box-sizing: border-box;
}

body {
  margin: 0;
  font-family: 'Inter', sans-serif;
  background: #F9FBFD;
  color: #333;
}

/* ================= HEADER ================= */
header {
  background: white;
  padding: 14px 18px;
  border-bottom: 1px solid #eee;
}

.logo img {
  height: 70px;
}

/* ================= TITLE ================= */
.site-title {
  text-align: center;
  padding: 18px 12px 10px;
}

.site-title h1 {
  margin: 0;
  font-family: 'Poppins', sans-serif;
  font-size: 36px;
  color: #0B3C5D;
}

.site-title p {
  margin-top: 6px;
  font-size: 18px;
  color: #16A085;
}

/* ================= SLIDER ================= */
.slider {
  height: 60vh;
  position: relative;
  overflow: hidden;
  margin-top: 10px;
}

.slide {
  position: absolute;
  inset: 0;
  background-size: cover;
  background-position: center;
  opacity: 0;
  transition: opacity 1s ease;
}

.slide.active {
  opacity: 1;
}

.overlay {
  background: rgba(11, 60, 93, 0.65);
  height: 100%;
  display: flex;
  align-items: center;
  padding-left: 8%;
  color: white;
}

.overlay h2 {
  font-family: 'Poppins', sans-serif;
  font-size: 32px;
  color: #2ECC71;
  margin-bottom: 8px;
}

.overlay p {
  max-width: 520px;
  font-size: 17px;
}

/* ================= BUTTONS ================= */
.buttons a {
  display: inline-block;
  margin-top: 12px;
  margin-right: 8px;
  padding: 9px 16px;
  background: #16A085;
  color: white;
  text-decoration: none;
  border-radius: 6px;
  font-size: 14px;
  transition: 0.3s;
}

.buttons a:hover {
  background: #138D75;
}

.buttons a.notice {
  background: #F4B400;
  color: #000;
}

/* ================= DOTS ================= */
.dots {
  position: absolute;
  bottom: 15px;
  left: 8%;
}

.dots span {
  margin-right: 8px;
  font-size: 16px;
  opacity: 0.5;
  color: white;
}

.dots span.active {
  opacity: 1;
  color: #2ECC71;
}

/* ================= SECTIONS ================= */
.sections {
  padding: 50px 8%;
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
  gap: 24px;
}

.card {
  background: white;
  padding: 26px;
  border-radius: 12px;
  box-shadow: 0 6px 15px rgba(0,0,0,0.08);
  transition: transform 0.3s, box-shadow 0.3s;
}

.card:hover {
  transform: translateY(-6px);
  box-shadow: 0 10px 20px rgba(0,0,0,0.12);
}

.card h3 {
  font-family: 'Poppins', sans-serif;
  color: #0B3C5D;
  margin-bottom: 10px;
}

/* ================= FOOTER ================= */
footer {
  background: #0B3C5D;
  color: #ddd;
  text-align: center;
  padding: 16px;
  font-size: 13px;
}

/* ================= MOBILE ================= */
@media (max-width: 600px) {
  .site-title h1 {
    font-size: 30px;
  }

  .overlay h2 {
    font-size: 26px;
  }

  .slider {
    height: 55vh;
  }
}
</style>
</head>

<body>

<header>
  <div class="logo">
    <img src="logo.png" alt="Medico Help Logo">
  </div>
</header>

<div class="site-title">
  <h1>Medico Help</h1>
  <p>One for all and all for one</p>
</div>

<section class="slider">

  <div class="slide active" style="background-image:url('slide1.jpg')">
    <div class="overlay">
      <div>
        <h2>Future Medicos</h2>
        <p>Clear guidance and resources for students dreaming of MBBS.</p>
        <div class="buttons">
          <a href="#">NEET UG</a>
          <a href="#" class="notice">Notices</a>
        </div>
      </div>
    </div>
  </div>

  <div class="slide" style="background-image:url('slide2.jpg')">
    <div class="overlay">
      <div>
        <h2>PG Aspirants</h2>
        <p>Smart preparation strategies for NEET PG and INICET.</p>
        <div class="buttons">
          <a href="#">NEET PG</a>
          <a href="#">INICET</a>
        </div>
      </div>
    </div>
  </div>

  <div class="slide" style="background-image:url('slide3.jpg')">
    <div class="overlay">
      <div>
        <h2>Clinical Career</h2>
        <p>Jobs, pathways and growth opportunities in medicine.</p>
        <div class="buttons">
          <a href="#">Jobs</a>
        </div>
      </div>
    </div>
  </div>

  <div class="slide" style="background-image:url('slide4.jpg')">
    <div class="overlay">
      <div>
        <h2>Future of Medicine</h2>
        <p>AI, innovation and evolving healthcare careers.</p>
        <div class="buttons">
          <a href="#">AI in Medicine</a>
        </div>
      </div>
    </div>
  </div>

  <div class="dots">
    <span class="active">1</span>
    <span>2</span>
    <span>3</span>
    <span>4</span>
  </div>

</section>

<section class="sections">
  <div class="card"><h3>About</h3><p>Built to guide, support and inspire every medico in India.</p></div>
  <div class="card"><h3>Exams</h3><p>NEET UG, NEET PG, INICET and regional exams.</p></div>
  <div class="card"><h3>Study Resources</h3><p>Books, notes, practicals and exam materials.</p></div>
  <div class="card"><h3>Important Notices</h3><p>Latest exam alerts, job updates and announcements.</p></div>
  <div class="card"><h3>Job Opportunities</h3><p>Career options during MBBS, after MBBS and after PG.</p></div>
</section>

<footer>
  Disclaimer: This site is just for information and helping purpose.
</footer>

<script>
let slides = document.querySelectorAll(".slide");
let dots = document.querySelectorAll(".dots span");
let index = 0;

setInterval(() => {
  slides[index].classList.remove("active");
  dots[index].classList.remove("active");
  index = (index + 1) % slides.length;
  slides[index].classList.add("active");
  dots[index].classList.add("active");
}, 5000);
</script>

</body>
</html>
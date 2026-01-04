<html lang="en">
<head>
<meta charset="UTF-8">
<title>Medico Help | One for all, all for one</title>
<link rel="icon" type="image/png" href="file_000000000e4072099451d53e35f73563.png">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<style>
body {
  margin: 0;
  font-family: Arial, sans-serif;
  background: #f2f5fa;
  color: #333;
}

/* HEADER */
header {
  background: linear-gradient(135deg, #0b5ed7, #20c997, #6f42c1);
  color: white;
  padding: 28px 15px;
  text-align: center;
}
header h1 {
  margin: 0;
  font-size: 34px;
}
header p {
  margin-top: 6px;
  font-style: italic;
}

/* NAV */
nav {
  background: white;
  display: flex;
  justify-content: center;
  flex-wrap: wrap;
  padding: 12px;
  box-shadow: 0 3px 8px rgba(0,0,0,0.1);
}
nav a {
  margin: 8px 14px;
  text-decoration: none;
  color: #0b5ed7;
  font-weight: bold;
}

/* IMAGE SLIDER */
.image-slider {
  width: 100%;
  height: 220px;
  overflow: hidden;
}
.image-slider img {
  width: 100%;
  height: 220px;
  object-fit: cover;
  display: none;
}
.image-slider img.active {
  display: block;
}

/* TEXT SLIDER */
.text-slider {
  background: linear-gradient(90deg, #e7f1ff, #fff3cd);
  text-align: center;
  padding: 18px;
  font-size: 18px;
  font-weight: bold;
}

/* SECTION */
section {
  background: white;
  margin: 16px;
  padding: 22px;
  border-radius: 12px;
  box-shadow: 0 5px 14px rgba(0,0,0,0.06);
}

section h2 {
  color: #0b5ed7;
  margin-top: 0;
}

/* CARDS */
.cards {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(150px, 1fr));
  gap: 16px;
}

.card {
  background: linear-gradient(135deg, #f1f6ff, #e8fff7);
  padding: 20px;
  text-align: center;
  border-radius: 14px;
  font-weight: bold;
  color: #0b5ed7;
}

/* FOOTER */
footer {
  background: linear-gradient(135deg, #212529, #343a40);
  color: #ddd;
  text-align: center;
  padding: 22px;
  font-size: 14px;
}
footer .disclaimer {
  font-size: 13px;
  color: #bbb;
  margin-top: 10px;
}
</style>

<script>
/* TEXT SLIDER */
const texts = [
  "📚 Smart study plans for Medicos",
  "🎯 Medical career scope & guidance",
  "🤖 AI and the future of Medicine",
  "📝 NEET UG | NEET PG | INI-CET updates",
  "💼 Job opportunities & notices"
];
let t = 0;
function changeText() {
  document.getElementById("textSlide").innerText = texts[t];
  t = (t + 1) % texts.length;
}
setInterval(changeText, 2500);

/* IMAGE SLIDER */
let imgIndex = 0;
function changeImage() {
  const images = document.querySelectorAll(".image-slider img");
  images.forEach(img => img.classList.remove("active"));
  images[imgIndex].classList.add("active");
  imgIndex = (imgIndex + 1) % images.length;
}
setInterval(changeImage, 3000);
</script>
</head>

<body onload="changeText(); changeImage();">

<header>
  <h1>Medico Help</h1>
  <p>One for all, all for one.</p>
</header>
<nav>
  <a href="#about">About</a>
  <a href="#exams">Exams</a>
  <a href="#resources">Study Resources</a>
  <a href="#notices">Notices</a>
  <a href="#jobs">Jobs</a>
</nav>

<div class="image-slider">
  <img src="https://images.unsplash.com/photo-1580281657527-47b2a3a0c9c3" class="active">
  <img src="https://images.unsplash.com/photo-1584433144859-1fc3ab64a957">
  <img src="https://images.unsplash.com/photo-1579684385127-1ef15d508118">
  <img src="https://images.unsplash.com/photo-1588776814546-1ffcf47267a5">
</div>

<div class="text-slider">
  <span id="textSlide"></span>
</div>

<section id="about">
  <h2>Welcome to Medico Help</h2>
  <p>
    Medico Help is a dedicated platform for those who dream to be medicos,
    are medicos, or admire the medical profession.
  </p>
  <p>
    Get reliable updates on exams, study resources, career scope,
    job opportunities, and important notices — all in one place.
  </p>
</section>

<section id="exams">
  <h2>Exams Covered</h2>
  <div class="cards">
    <div class="card">NEET UG</div>
    <div class="card">NEET PG</div>
    <div class="card">INI-CET</div>
    <div class="card">Regional Exams</div>
  </div>
</section>

<section id="resources">
  <h2>Study Resources</h2>
  <div class="cards">
    <div class="card">Books</div>
    <div class="card">Practical Notes</div>
    <div class="card">Exam Notes</div>
    <div class="card">Job Resources</div>
  </div>
</section>

<section id="notices">
  <h2>Important Notices</h2>
  <div class="cards">
    <div class="card">Exam Notices</div>
    <div class="card">Job Notices</div>
    <div class="card">Other Updates</div>
  </div>
</section>

<section id="jobs">
  <h2>Job Opportunities</h2>
  <div class="cards">
    <div class="card">During MBBS</div>
    <div class="card">After MBBS</div>
    <div class="card">After PG</div>
  </div>
</section>

<footer>
  © 2026 Medico Help | medicohelp.in
  <div class="disclaimer">
    Disclaimer: This website is created solely for informational and helping purposes.
    It does not replace professional medical advice or official notifications.
  </div>
</footer>

</body>
</html>
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>Medico Help | One for all, all for one</title>
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<style>
body {
  margin: 0;
  font-family: Arial, sans-serif;
  background: #f4f7fb;
  color: #333;
}

/* HEADER */
header {
  background: linear-gradient(135deg, #0b5ed7, #084298);
  color: white;
  padding: 25px 15px;
  text-align: center;
}
header h1 {
  margin: 0;
  font-size: 32px;
}
header p {
  margin-top: 6px;
  font-style: italic;
  opacity: 0.95;
}

/* NAV */
nav {
  background: white;
  display: flex;
  justify-content: center;
  flex-wrap: wrap;
  padding: 10px;
  box-shadow: 0 2px 6px rgba(0,0,0,0.1);
}
nav a {
  margin: 8px 12px;
  text-decoration: none;
  color: #0b5ed7;
  font-weight: bold;
}

/* SLIDER */
.slider {
  background: #e7f1ff;
  text-align: center;
  padding: 22px;
  font-size: 18px;
  font-weight: bold;
}

/* SECTION */
section {
  background: white;
  margin: 14px;
  padding: 20px;
  border-radius: 10px;
  box-shadow: 0 4px 10px rgba(0,0,0,0.05);
}

section h2 {
  color: #0b5ed7;
  margin-top: 0;
}

/* CARDS */
.cards {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(150px, 1fr));
  gap: 15px;
}

.card {
  background: #f1f6ff;
  padding: 18px;
  text-align: center;
  border-radius: 10px;
  font-weight: bold;
  color: #0b5ed7;
}

/* DISCLAIMER */
.disclaimer {
  font-size: 13px;
  color: #777;
  border-top: 1px solid #ddd;
  margin-top: 15px;
  padding-top: 10px;
}

/* FOOTER */
footer {
  text-align: center;
  padding: 15px;
  font-size: 14px;
  color: #666;
}
</style>

<script>
const slides = [
  "📚 Smart study plans for Medicos",
  "🎯 Scope & future in Medical career",
  "🤖 Role of AI in Medicine",
  "📝 NEET UG | NEET PG | INI-CET updates",
  "📢 Important notices & counselling alerts",
  "💼 Job opportunities for Medicos"
];
let i = 0;
function slideShow() {
  document.getElementById("slide").innerText = slides[i];
  i = (i + 1) % slides.length;
}
setInterval(slideShow, 2500);
</script>
</head>

<body onload="slideShow()">

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

<div class="slider">
  <span id="slide"></span>
</div>

<section>
  <h2>Welcome to Medico Help</h2>
  <p>
    A single platform created to support those who dream to be medicos,
    are medicos, or love the medical profession.
  </p>
  <p>
    We provide reliable updates on exams, career guidance, study resources,
    job opportunities, and important notices — all in one place.
  </p>
  <div class="disclaimer">
    Disclaimer: This site is just for information and helping purpose.
  </div>
</section>

<section id="exams">
  <h2>Exams Covered</h2>
  <div class="cards">
    <div class="card">NEET UG</div>
    <div class="card">NEET PG</div>
    <div class="card">INI-CET</div>
    <div class="card">Regional Exams</div>
  </div>
  <div class="disclaimer">This site is just for information and helping purpose.</div>
</section>

<section id="resources">
  <h2>Study Resources</h2>
  <div class="cards">
    <div class="card">Books</div>
    <div class="card">Practical Notes</div>
    <div class="card">Exam Notes</div>
    <div class="card">Job Resources</div>
  </div>
  <div class="disclaimer">This site is just for information and helping purpose.</div>
</section>

<section id="notices">
  <h2>Important Notices</h2>
  <div class="cards">
    <div class="card">Exam Notices</div>
    <div class="card">Job Notices</div>
    <div class="card">Others</div>
  </div>
  <div class="disclaimer">This site is just for information and helping purpose.</div>
</section>

<section id="jobs">
  <h2>Job Opportunities</h2>
  <div class="cards">
    <div class="card">During MBBS</div>
    <div class="card">After MBBS</div>
    <div class="card">After PG</div>
  </div>
  <div class="disclaimer">This site is just for information and helping purpose.</div>
</section>

<footer>
  © 2026 Medico Help | medicohelp.in
</footer>

</body>
</html>
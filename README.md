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
  background: #f4f6f9;
  color: #333;
}
header {
  background: #0b5ed7;
  color: white;
  text-align: center;
  padding: 20px;
}
header h1 {
  margin: 0;
}
header p {
  margin: 5px 0 0;
  font-style: italic;
}

nav {
  background: #ffffff;
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  padding: 10px;
  box-shadow: 0 2px 4px rgba(0,0,0,0.1);
}
nav a {
  margin: 8px 12px;
  text-decoration: none;
  color: #0b5ed7;
  font-weight: bold;
}

.slider {
  background: #e9f2ff;
  padding: 25px;
  text-align: center;
  font-size: 18px;
  font-weight: bold;
}

section {
  background: white;
  margin: 12px;
  padding: 20px;
  border-radius: 8px;
}

h2 {
  color: #0b5ed7;
}

ul {
  padding-left: 20px;
}

.disclaimer {
  font-size: 13px;
  color: #777;
  border-top: 1px solid #ddd;
  margin-top: 15px;
  padding-top: 10px;
}

footer {
  text-align: center;
  padding: 15px;
  font-size: 14px;
  color: #666;
}
</style>

<script>
const slides = [
  "📚 Smart Study Plans for Medicos",
  "🎯 Scope & Career Guidance in Medical Field",
  "🤖 Future of AI in Medicine",
  "📝 Latest Medical Exams & Updates",
  "💼 Job Opportunities for Medicos",
  "📌 Important Notices & Resources"
];
let index = 0;
function changeSlide() {
  document.getElementById("slideText").innerText = slides[index];
  index = (index + 1) % slides.length;
}
setInterval(changeSlide, 2500);
</script>
</head>

<body onload="changeSlide()">

<header>
  <h1>Medico Help</h1>
  <p>One for all, all for one.</p>
</header>

<nav>
  <a href="#about">About</a>
  <a href="#exams">Exams</a>
  <a href="#study">Study Resource</a>
  <a href="#notice">Important Notices</a>
  <a href="#jobs">Job Opportunities</a>
</nav>

<div class="slider">
  <span id="slideText"></span>
</div>

<section id="about">
  <h2>About</h2>
  <p>
    This website is solely functional to help everyone who dreamt to be a medico,
    is a medico, or loves medico.
  </p>
  <p>
    You will get updated news, exam notices, tips, tricks, job opportunities,
    resources, and help related to the medical field.
  </p>
  <div class="disclaimer">
    Disclaimer: This site is just for information and helping purpose.
  </div>
</section>

<section id="exams">
  <h2>Exams</h2>
  <ul>
    <li><strong>NEET UG</strong></li>
    <li><strong>NEET PG</strong></li>
    <li><strong>INI-CET</strong></li>
    <li><strong>Regional Job Related Exams</strong></li>
  </ul>
  <div class="disclaimer">
    Disclaimer: This site is just for information and helping purpose.
  </div>
</section>

<section id="study">
  <h2>Study Resource</h2>
  <ul>
    <li><strong>Books</strong></li>
    <li><strong>Practical Notes</strong></li>
    <li><strong>Exam Related Notes</strong></li>
    <li><strong>Job Related Resources</strong></li>
  </ul>
  <div class="disclaimer">
    Disclaimer: This site is just for information and helping purpose.
  </div>
</section>

<section id="notice">
  <h2>Important Notices</h2>
  <ul>
    <li><strong>Exam Related Notices</strong></li>
    <li><strong>Job Related Notices</strong></li>
    <li><strong>Others</strong></li>
  </ul>
  <div class="disclaimer">
    Disclaimer: This site is just for information and helping purpose.
  </div>
</section>

<section id="jobs">
  <h2>Job Opportunities</h2>
  <ul>
    <li><strong>During MBBS</strong></li>
    <li><strong>Just After MBBS</strong></li>
    <li><strong>After PG</strong></li>
  </ul>
  <div class="disclaimer">
    Disclaimer: This site is just for information and helping purpose.
  </div>
</section>

<footer>
  © 2026 Medico Help | medicohelp.in
</footer>

</body>
</html># medicohelp.github.io

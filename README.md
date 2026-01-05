<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Medico Help | One for all and all for one</title>

<link href="https://fonts.googleapis.com/css2?family=Poppins:wght@600;700&family=Inter:wght@400;500&display=swap" rel="stylesheet">

<style>
:root {
  --bg: #F9FBFD;
  --card: #ffffff;
  --text: #333;
  --primary: #0B3C5D;
  --accent: #16A085;
}

body.dark {
  --bg: #0E1621;
  --card: #162235;
  --text: #E5E7EB;
  --primary: #60A5FA;
  --accent: #2ECC71;
}

* {
  box-sizing: border-box;
  transition: background 0.3s, color 0.3s;
}

body {
  margin: 0;
  font-family: 'Inter', sans-serif;
  background: var(--bg);
  color: var(--text);
}

/* ================= HEADER ================= */
header {
  background: var(--card);
  padding: 14px 18px;
  border-bottom: 1px solid rgba(0,0,0,0.08);
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.logo img {
  height: 70px;
}

/* ================= TOGGLE ================= */
.toggle {
  cursor: pointer;
  background: var(--accent);
  color: white;
  padding: 6px 14px;
  border-radius: 20px;
  font-size: 14px;
  user-select: none;
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
  color: var(--primary);
}

.site-title p {
  margin-top: 6px;
  font-size: 18px;
  color: var(--accent);
}

/* ================= SLIDER ================= */
.slider {
  height: 58vh;
  position: relative;
  overflow: hidden;
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
  background: rgba(0,0,0,0.55);
  height: 100%;
  display: flex;
  align-items: center;
  padding-left: 8%;
  color: white;
}

.overlay h2 {
  font-family: 'Poppins', sans-serif;
  font-size: 32px;
  color: var(--accent);
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
  background: var(--accent);
  color: white;
  text-decoration: none;
  border-radius: 6px;
  font-size: 14px;
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
  color: var(--accent);
}

/* ================= SECTIONS ================= */
.sections {
  padding: 50px 8%;
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
  gap: 24px;
}

.card {
  background: var(--card);
  padding: 26px;
  border-radius: 12px;
  box-shadow: 0 6px 15px rgba(0,0,0,0.1);
}

.card h3 {
  font-family: 'Poppins', sans-serif;
  color: var(--primary);
}

/* ================= FOOTER ================= */
footer {
  background: var(--primary);
  color: white;
  text-align: center;
  padding: 16px;
  font-size: 13px;
}

/* ================= MOBILE ================= */
@media (max-width: 600px) {
  .site-title h1 { font-size: 30px; }
  .overlay h2 { font-size: 26px; }
}
</style>
</head>

<body>

<header>
  <div class="logo">
    <img src="logo.png" alt="Medico Help Logo">
  </div>
  <div class="toggle" onclick="toggleMode()">🌙 / ☀️</div>
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
      </div>
    </div>
  </div>
  <div class="slide" style="background-image:url('slide2.jpg')">
    <div class="overlay">
      <div>
        <h2>PG Aspirants</h2>
        <p>Smart strategies for NEET PG and INICET.</p>
      </div>
    </div>
  </div>
</section>

<section class="sections">
  <div class="card"><h3>About</h3><p>Helping medicos at every stage.</p></div>
  <div class="card"><h3>Exams</h3><p>UG, PG & superspeciality guidance.</p></div>
  <div class="card"><h3>Resources</h3><p>Notes, books and preparation tools.</p></div>
</section>

<footer>
  Disclaimer: This site is for information and helping purpose only.
</footer>

<script>
let slides = document.querySelectorAll(".slide");
let dots = document.querySelectorAll(".dots span");
let i = 0;

setInterval(() => {
  slides[i].classList.remove("active");
  i = (i + 1) % slides.length;
  slides[i].classList.add("active");
}, 5000);

// DARK MODE
function toggleMode() {
  document.body.classList.toggle("dark");
  localStorage.setItem("theme",
    document.body.classList.contains("dark") ? "dark" : "light"
  );
}

// LOAD SAVED MODE
if (localStorage.getItem("theme") === "dark") {
  document.body.classList.add("dark");
}
</script>

</body>
</html>
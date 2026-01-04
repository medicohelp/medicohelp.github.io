<html lang="en">

<style>
* { box-sizing: border-box; }

body, html {
  margin: 0;
  font-family: Arial, sans-serif;
}

/* ================= HEADER ================= */
header {
  padding: 12px 16px;
  background: white;
}

.logo img {
  height: 70px;
  width: auto;
}

/* ================= TITLE AREA ================= */
.site-title {
  text-align: center;
  padding: 12px 10px 6px;
}

.site-title h1 {
  margin: 0;
  font-family: 'Poppins', sans-serif;
  font-size: 34px;
  color: #0B3C5D;
  letter-spacing: 1px;
}

.site-title p {
  margin: 4px 0 0;
  font-family: 'Playfair Display', serif;
  font-size: 18px;
  color: #1ABC9C;
}

/* ================= SLIDER ================= */
.slider {
  height: 65vh; /* SMALLER HERO */
  position: relative;
  overflow: hidden;
}

.slide {
  position: absolute;
  inset: 0;
  background-size: cover;
  background-position: center;
  opacity: 0;
  transition: opacity 1s ease-in-out;
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
  font-size: 34px;
  color: #2ECC71;
  margin-bottom: 8px;
}

.overlay p {
  font-size: 18px;
  max-width: 520px;
}

/* ================= BUTTONS ================= */
.buttons a {
  display: inline-block;
  margin-top: 12px;
  margin-right: 10px;
  padding: 9px 16px;
  background: #1ABC9C;
  color: white;
  text-decoration: none;
  border-radius: 4px;
  font-size: 14px;
}

.buttons a.notice {
  background: #F39C12;
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
  padding: 45px 8%;
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
  gap: 20px;
  background: #f5f7fa;
}

.card {
  background: white;
  padding: 22px;
  border-radius: 8px;
  box-shadow: 0 4px 10px rgba(0,0,0,0.1);
}

.card h3 {
  color: #0B3C5D;
}

/* ================= FOOTER ================= */
footer {
  background: #0B3C5D;
  color: #ccc;
  text-align: center;
  padding: 14px;
  font-size: 13px;
}

/* ================= MOBILE ================= */
@media (max-width: 600px) {
  .logo img {
    height: 60px;
  }

  .site-title h1 {
    font-size: 30px;
  }

  .overlay h2 {
    font-size: 28px;
  }

  .slider {
    height: 60vh;
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
        <p>Guidance, resources and clarity for every student dreaming of MBBS.</p>
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
        <h2>Postgraduate Aspirants</h2>
        <p>NEET PG & INICET preparation with smart study plans.</p>
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
        <h2>Clinical Journey</h2>
        <p>From MBBS to PG and beyond — career guidance at every step.</p>
        <div class="buttons">
          <a href="#">Jobs</a>
          <a href="#" class="notice">Updates</a>
        </div>
      </div>
    </div>
  </div>

  <div class="slide" style="background-image:url('slide4.jpg')">
    <div class="overlay">
      <div>
        <h2>Future of Medicine</h2>
        <p>AI, technology and evolving opportunities in healthcare.</p>
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
  <div class="card"><h3>About</h3><p>Dedicated to everyone who dreams, studies and lives medicine.</p></div>
  <div class="card"><h3>Exams</h3><p>NEET UG, NEET PG, INICET & regional exams.</p></div>
  <div class="card"><h3>Study Resources</h3><p>Books, notes, practicals and exam material.</p></div>
  <div class="card"><h3>Important Notices</h3><p>Exam alerts, job updates and announcements.</p></div>
  <div class="card"><h3>Job Opportunities</h3><p>During MBBS, after MBBS and post-PG careers.</p></div>
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
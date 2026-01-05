<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Medico Help | One for all and all for one</title>
  <meta name="viewport" content="width=device-width, initial-scale=1.0">

  <!-- SEO -->
  <meta name="description" content="Medico Help is a trusted platform for NEET UG, NEET PG, INICET, medical exams, jobs and study resources in India.">
  <meta name="keywords" content="NEET UG, NEET PG, INICET, medical jobs, MBBS notes, medico help">
  <meta name="author" content="Medico Help">

  <!-- Fonts -->
  <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@600;700&family=Inter:wght@400;500&display=swap" rel="stylesheet">

  <style>
    :root{
      --primary:#0B3C5D;
      --accent:#16A085;
      --bg:#F9FBFD;
      --text:#2b2b2b;
    }

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
      background:#fff;
      display:flex;
      align-items:center;
      justify-content:space-between;
      padding:12px 6%;
      box-shadow:0 2px 10px rgba(0,0,0,0.08);
    }

    nav img{
      height:65px;
    }

    nav ul{
      list-style:none;
      display:flex;
      gap:22px;
      padding:0;
      margin:0;
    }

    nav a{
      text-decoration:none;
      color:var(--text);
      font-weight:500;
    }

    nav a:hover{
      color:var(--accent);
    }

    .nav-btn{
      background:var(--accent);
      color:#fff;
      padding:8px 16px;
      border-radius:22px;
      text-decoration:none;
      font-size:14px;
    }

    /* ================= HERO SLIDER ================= */
    .hero{
      height:65vh;
      position:relative;
      overflow:hidden;
    }

    .slide{
      position:absolute;
      inset:0;
      background-size:cover;
      background-position:center;
      opacity:0;
      transition:opacity 1.2s ease;
    }

    .slide.active{
      opacity:1;
    }

    .overlay{
      height:100%;
      background:rgba(0,0,0,0.55);
      display:flex;
      align-items:center;
      padding-left:8%;
    }

    .hero-text h1{
      font-family:'Poppins',sans-serif;
      font-size:46px;
      color:#fff;
      margin-bottom:6px;
    }

    .hero-text h2{
      font-size:20px;
      color:var(--accent);
      margin-top:0;
    }

    .hero-text p{
      max-width:520px;
      color:#ddd;
      font-size:16px;
      margin-top:12px;
    }

    /* ================= SEARCH ================= */
    .search-box{
      margin-top:18px;
    }

    .search-box input{
      padding:12px 18px;
      width:300px;
      border-radius:25px;
      border:none;
      outline:none;
      font-size:14px;
    }

    /* ================= ABOUT ================= */
    .about{
      padding:55px 10%;
      text-align:center;
    }

    .about h3{
      font-family:'Poppins',sans-serif;
      font-size:28px;
      color:var(--primary);
    }

    .about p{
      max-width:850px;
      margin:auto;
      font-size:16px;
      line-height:1.7;
    }

    /* ================= FOOTER ================= */
    footer{
      background:var(--primary);
      color:#fff;
      padding:15px;
      text-align:center;
      font-size:13px;
    }

    /* ================= MOBILE ================= */
    @media(max-width:600px){
      nav ul{display:none;}
      .hero-text h1{font-size:34px;}
      .search-box input{width:240px;}
    }
  </style>
</head>

<body>

<!-- NAVBAR -->
<nav>
  <img src="images/logo.png" alt="Medico Help Logo">
  <ul>
    <li><a href="index.html">Home</a></li>
    <li><a href="about.html">About</a></li>
    <li><a href="exams.html">Exams</a></li>
    <li><a href="resources.html">Resources</a></li>
    <li><a href="jobs.html">Jobs</a></li>
    <li><a href="notices.html">Notices</a></li>
  </ul>
  <a href="login.html" class="nav-btn">Login</a>
</nav>

<!-- HERO -->
<section class="hero">
  <div class="slide active" style="background-image:url('images/slide1.jpg')">
    <div class="overlay">
      <div class="hero-text">
        <h1>Medico Help</h1>
        <h2>One for all and all for one</h2>
        <p>
          A trusted companion for every medico — from aspirant to professional.
        </p>

        <div class="search-box">
          <input type="text" placeholder="Search exams, jobs, notes...">
        </div>
      </div>
    </div>
  </div>

  <div class="slide" style="background-image:url('images/slide2.jpg')">
    <div class="overlay">
      <div class="hero-text">
        <h1>Guidance. Resources. Growth.</h1>
        <h2>Built for Indian Medicos</h2>
        <p>
          Clear information, genuine help, and a community-first approach.
        </p>
      </div>
    </div>
  </div>
</section>

<!-- ABOUT -->
<section class="about">
  <h3>About Medico Help</h3>
  <p>
    Medico Help is created to support every student and doctor who dreams of
    serving society through medicine. From exam guidance to career opportunities,
    this platform aims to provide clear, reliable, and ethical medical information
    for Indian medicos.
  </p>
</section>

<!-- FOOTER -->
<footer>
  Disclaimer: This site is for information and helping purpose only.
</footer>

<script>
  let slides = document.querySelectorAll('.slide');
  let index = 0;

  setInterval(() => {
    slides[index].classList.remove('active');
    index = (index + 1) % slides.length;
    slides[index].classList.add('active');
  }, 5000);
</script>

</body>
</html>
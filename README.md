<!DOCTYPE html>
<html lang="th">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1" />
<title>Portfolio ของฉัน</title>
<style>
  body {
    margin: 0;
    font-family: sans-serif;
    background: #f9f9f9;
  }

  .menu-toggle {
    position: fixed;
    top: 20px;
    left: 20px;
    width: 40px;
    height: 40px;
    background-color: rgba(0,0,0,0.5);
    color: white;
    border: none;
    font-size: 28px;
    z-index: 1100;
    cursor: pointer;
    border-radius: 5px;
    display: flex;
    align-items: center;
    justify-content: center;
    transition: background-color 0.3s ease;
  }
  .menu-toggle:hover {
    background-color: rgba(0,0,0,0.8);
  }

  .sidebar {
    position: fixed;
    top: 0;
    left: 0;
    width: 220px;
    height: 100%;
    background: #222;
    color: #fff;
    padding-top: 60px;
    z-index: 1050;
    transition: transform 0.3s ease;
    transform: translateX(-100%);
    box-shadow: 3px 0 8px rgba(0,0,0,0.3);
  }

  .sidebar.show {
    transform: translateX(0);
  }

  .sidebar ul {
    list-style: none;
    padding: 0;
    margin: 0;
  }

  .sidebar li {
    margin: 20px 0;
    text-align: center;
  }

  .sidebar a {
    color: #fff;
    text-decoration: none;
    font-size: 18px;
    display: block;
    padding: 10px 0;
    transition: background 0.2s;
  }

  .sidebar a:hover {
    background: #444;
  }

  header {
    position: relative;
    width: 100vw;
    height: 100vh;
    overflow: hidden;
  }

  .slider {
    position: absolute;
    top: 0;
    left: 0;
    width: 100vw;
    height: 100vh;
  }

  .slider img {
    position: absolute;
    top: 0;
    left: 0;
    width: 100vw;
    height: 100vh;
    object-fit: cover;
    opacity: 0;
    transition: opacity 1s ease;
  }

  .slider img.active {
    opacity: 1;
  }

  .header-text {
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    color: white;
    text-align: center;
    text-shadow: 2px 2px 8px rgba(0, 0, 0, 0.7);
    z-index: 10;
    padding: 20px;
    background-color: rgba(0, 0, 0, 0.3);
    border-radius: 12px;
  }

  .header-text h1 {
    font-size: 48px;
    margin-bottom: 10px;
  }

  .header-text p {
    font-size: 20px;
  }

  section {
    padding: 30px;
    max-width: 1000px;
    margin: 40px auto;
    display: none;
  }

  section.active {
    display: block;
  }

  /* Skills section image grid */
  .skills-gallery {
    display: flex;
    flex-wrap: wrap;
    gap: 20px;
    margin-top: 20px;
    justify-content: center;
  }

  .skill-item {
    position: relative;
    width: 240px;
    overflow: hidden;
    border-radius: 12px;
    cursor: pointer;
    transition: transform 0.3s ease;
  }

  .skill-item img {
    width: 100%;
    height: auto;
    display: block;
    border-radius: 12px;
    transition: transform 0.3s ease;
  }

  .skill-item:hover img {
    transform: scale(1.05);
  }

  .skill-info {
    position: absolute;
    bottom: 0;
    left: 0;
    right: 0;
    background: rgba(0,0,0,0.6);
    color: white;
    padding: 10px;
    font-size: 14px;
    text-align: center;
    opacity: 0;
    transition: opacity 0.3s ease;
  }

  .skill-item:hover .skill-info {
    opacity: 1;
  }

  .contact-cards {
    display: flex;
    flex-wrap: wrap;
    gap: 20px;
    justify-content: center;
    margin-top: 20px;
  }

  .contact-card {
    flex: 1 1 200px;
    max-width: 250px;
    background: #ffffff;
    border-radius: 12px;
    padding: 20px;
    text-align: center;
    box-shadow: 0 4px 10px rgba(0,0,0,0.1);
    cursor: pointer;
    transition: transform 0.3s ease, box-shadow 0.3s ease;
  }

  .contact-card:hover {
    transform: translateY(-5px);
    box-shadow: 0 8px 16px rgba(0,0,0,0.2);
  }

  .contact-card img {
    width: 40px;
    height: 40px;
    margin-bottom: 10px;
  }

  .contact-card p {
    margin: 0;
    font-size: 16px;
    color: #333;
  }

  .contact-card.email { background-color: #e8f5e9; }
  .contact-card.line { background-color: #e0f7fa; }
  .contact-card.instagram { background-color: #fce4ec; }
  .contact-card.phone { background-color: #f3e5f5; }

  @media (max-width: 768px) {
    .menu-toggle {
      width: 35px;
      height: 35px;
      font-size: 24px;
    }

    .sidebar {
      width: 180px;
    }

    .contact-card {
      flex: 1 1 100%;
    }
  }
</style>
</head>
<body>

<button class="menu-toggle" aria-label="Toggle menu" onclick="toggleSidebar()">☰</button>

<nav class="sidebar" id="sidebar">
  <ul>
    <li><a href="#about">เกี่ยวกับฉัน</a></li>
    <li><a href="#skills">ความสามารถพิเศษ</a></li>
    <li><a href="#contact">ช่องทางการติดต่อ</a></li>
  </ul>
</nav>

<header id="main-header">
  <div class="slider">
    <img src="me1.jpg" class="active" alt="รูปที่ 1" />
    <img src="3.jpg" alt="รูปที่ 3" />
    <img src="5.jpg" alt="รูปที่ 5" />
    <img src="6.jpg" alt="รูปที่ 6" />
  </div>
  <div class="header-text">
    <h1>Welcome to my Portfolio</h1>
    <p>Thitiwoot Sompong</p>
  </div>
</header>

<section id="about">
  <h2>เกี่ยวกับฉัน</h2>
  <p>
    Name: Thitiwoot Sompong<br />
    Age: 17<br />
    Birthday: 24/06/2008<br />
    Class: 5/1<br />
    School: Rattanaratbumrung School
  </p>
</section>

<section id="skills">
  <h2>ผลงานทางวิชาการและกิจกรรมที่เข้าร่วม</h2>
  <ul>
    <li>Thailand Robot & Coding Challenge</li>
  </ul>
  <div class="skills-gallery">
    <div class="skill-item" onclick="alert('การแข่งขัน Thailand Robot & Coding Challenge 2024 ระดับประเทศ')">
      <img src="robot.jpg" alt="Robot Event">
      <div class="skill-info">Thailand Robot Challenge</div>
    </div>
    <div class="skill-item" onclick="alert('กิจกรรม Coding Camp ที่จังหวัดขอนแก่น')">
      <img src="coding.jpg" alt="Coding Event">
      <div class="skill-info">Coding Camp</div>
    </div>
  </div>
</section>

<section id="contact">
  <h2>ช่องทางการติดต่อ</h2>
  <div class="contact-cards">
    <div class="contact-card email" onclick="window.location.href='mailto:40874@rr.ac.th'">
      <img src="https://cdn.jsdelivr.net/gh/simple-icons/simple-icons/icons/maildotru.svg" alt="Email" />
      <p>40874@rr.ac.th</p>
    </div>
    <div class="contact-card line" onclick="window.open('https://line.me/ti/p/~0983529390', '_blank')">
      <img src="https://cdn.jsdelivr.net/gh/simple-icons/simple-icons/icons/line.svg" alt="Line" />
      <p>0983529390</p>
    </div>
    <div class="contact-card instagram" onclick="window.open('https://instagram.com/_ttwsp', '_blank')">
      <img src="https://cdn.jsdelivr.net/gh/simple-icons/simple-icons/icons/instagram.svg" alt="Instagram" />
      <p>@_ttwsp</p>
    </div>
    <div class="contact-card phone">
      <img src="https://cdn.jsdelivr.net/gh/simple-icons/simple-icons/icons/phone.svg" alt="Phone" />
      <p>098-352-9390</p>
    </div>
  </div>
</section>

<script>
  function toggleSidebar() {
    document.getElementById('sidebar').classList.toggle('show');
  }

  function showSection(id) {
    document.querySelectorAll('section').forEach(sec => {
      sec.classList.remove('active');
    });
    const activeSection = document.getElementById(id);
    if (activeSection) {
      activeSection.classList.add('active');
      window.scrollTo(0, 0);
    }
  }

  document.querySelectorAll('.sidebar a').forEach(link => {
    link.addEventListener('click', function(e) {
      const targetId = this.getAttribute('href').substring(1);
      showSection(targetId);
      e.preventDefault();
      toggleSidebar();
    });
  });

  showSection('about');

  const slides = document.querySelectorAll('.slider img');
  let currentIndex = 0;

  setInterval(() => {
    slides[currentIndex].classList.remove('active');
    currentIndex = (currentIndex + 1) % slides.length;
    slides[currentIndex].classList.add('active');
  }, 3000);
</script>

</body>
</html>

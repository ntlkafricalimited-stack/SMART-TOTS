<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Smart Tots Kindergarten & Junior School</title>
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700;800&display=swap" rel="stylesheet">
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
      font-family: 'Poppins', sans-serif;
    }

    body {
      background: #f6fbff;
      color: #1d3557;
      overflow-x: hidden;
    }

    header {
      position: fixed;
      width: 100%;
      top: 0;
      z-index: 1000;
      background: rgba(255,255,255,0.92);
      backdrop-filter: blur(12px);
      box-shadow: 0 2px 20px rgba(0,0,0,0.08);
    }

    nav {
      display: flex;
      justify-content: space-between;
      align-items: center;
      padding: 18px 8%;
    }

    .logo {
      font-size: 28px;
      font-weight: 800;
      color: #0b5ed7;
    }

    .logo span {
      color: #ff7b00;
    }

    nav ul {
      display: flex;
      list-style: none;
      gap: 28px;
    }

    nav ul li a {
      text-decoration: none;
      color: #1d3557;
      font-weight: 500;
      transition: 0.3s;
    }

    nav ul li a:hover {
      color: #0b5ed7;
    }

    .hero {
      min-height: 100vh;
      display: flex;
      align-items: center;
      justify-content: space-between;
      padding: 140px 8% 80px;
      background: linear-gradient(135deg,#dff3ff,#fff7f0);
      gap: 50px;
    }

    .hero-text {
      flex: 1;
    }

    .hero-text h1 {
      font-size: 64px;
      line-height: 1.1;
      margin-bottom: 20px;
      color: #123c69;
    }

    .hero-text h1 span {
      color: #ff7b00;
    }

    .hero-text p {
      font-size: 18px;
      line-height: 1.8;
      margin-bottom: 30px;
      color: #456;
    }

    .hero-buttons {
      display: flex;
      gap: 20px;
      flex-wrap: wrap;
    }

    .btn {
      padding: 15px 28px;
      border-radius: 50px;
      text-decoration: none;
      font-weight: 600;
      transition: 0.3s;
      display: inline-block;
    }

    .primary {
      background: linear-gradient(135deg,#0b5ed7,#00a6ff);
      color: white;
      box-shadow: 0 10px 25px rgba(11,94,215,0.3);
    }

    .primary:hover {
      transform: translateY(-4px);
    }

    .secondary {
      border: 2px solid #0b5ed7;
      color: #0b5ed7;
    }

    .secondary:hover {
      background: #0b5ed7;
      color: white;
    }

    .hero-image {
      flex: 1;
      position: relative;
    }

    .hero-image img {
      width: 100%;
      border-radius: 30px;
      box-shadow: 0 25px 40px rgba(0,0,0,0.15);
    }

    .floating-card {
      position: absolute;
      background: white;
      padding: 18px;
      border-radius: 20px;
      box-shadow: 0 15px 25px rgba(0,0,0,0.12);
    }

    .card1 {
      top: -20px;
      left: -20px;
    }

    .card2 {
      bottom: -20px;
      right: -10px;
    }

    section {
      padding: 100px 8%;
    }

    .section-title {
      text-align: center;
      margin-bottom: 60px;
    }

    .section-title h2 {
      font-size: 44px;
      color: #123c69;
      margin-bottom: 15px;
    }

    .section-title p {
      color: #567;
      max-width: 700px;
      margin: auto;
      line-height: 1.7;
    }

    .features {
      display: grid;
      grid-template-columns: repeat(auto-fit,minmax(260px,1fr));
      gap: 30px;
    }

    .feature-box {
      background: white;
      border-radius: 24px;
      padding: 35px;
      transition: 0.4s;
      box-shadow: 0 10px 25px rgba(0,0,0,0.06);
    }

    .feature-box:hover {
      transform: translateY(-10px);
      box-shadow: 0 18px 35px rgba(0,0,0,0.12);
    }

    .feature-box h3 {
      margin: 20px 0 15px;
      color: #0b5ed7;
    }

    .feature-box p {
      line-height: 1.7;
      color: #555;
    }

    .feature-icon {
      width: 70px;
      height: 70px;
      background: linear-gradient(135deg,#0b5ed7,#00bfff);
      border-radius: 18px;
      display: flex;
      align-items: center;
      justify-content: center;
      color: white;
      font-size: 28px;
      font-weight: bold;
    }

    .gallery {
      display: grid;
      grid-template-columns: repeat(auto-fit,minmax(250px,1fr));
      gap: 20px;
    }

    .gallery img {
      width: 100%;
      height: 280px;
      object-fit: cover;
      border-radius: 24px;
      transition: 0.4s;
      box-shadow: 0 10px 25px rgba(0,0,0,0.08);
    }

    .gallery img:hover {
      transform: scale(1.03);
    }

    .news-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit,minmax(300px,1fr));
      gap: 30px;
    }

    .news-card {
      background: white;
      border-radius: 24px;
      overflow: hidden;
      box-shadow: 0 12px 25px rgba(0,0,0,0.08);
    }

    .news-card img {
      width: 100%;
      height: 220px;
      object-fit: cover;
    }

    .news-content {
      padding: 25px;
    }

    .news-content h3 {
      margin-bottom: 12px;
      color: #123c69;
    }

    .news-content p {
      line-height: 1.7;
      color: #555;
      margin-bottom: 15px;
    }

    .events {
      background: linear-gradient(135deg,#0b5ed7,#00a6ff);
      border-radius: 40px;
      color: white;
      padding: 70px;
      margin-top: 40px;
    }

    .event-list {
      display: grid;
      grid-template-columns: repeat(auto-fit,minmax(240px,1fr));
      gap: 25px;
      margin-top: 40px;
    }

    .event-item {
      background: rgba(255,255,255,0.15);
      padding: 25px;
      border-radius: 22px;
      backdrop-filter: blur(8px);
    }

    .event-item h4 {
      margin-bottom: 10px;
      font-size: 22px;
    }

    .online-classes {
      display: grid;
      grid-template-columns: repeat(auto-fit,minmax(320px,1fr));
      gap: 30px;
      align-items: center;
    }

    .online-classes img {
      width: 100%;
      border-radius: 30px;
      box-shadow: 0 15px 30px rgba(0,0,0,0.12);
    }

    .class-info ul {
      margin-top: 20px;
      list-style: none;
    }

    .class-info ul li {
      margin-bottom: 14px;
      padding-left: 25px;
      position: relative;
      color: #456;
    }

    .class-info ul li::before {
      content: '✔';
      position: absolute;
      left: 0;
      color: #0b5ed7;
      font-weight: bold;
    }

    .pta-section {
      background: white;
      border-radius: 35px;
      padding: 60px;
      box-shadow: 0 15px 35px rgba(0,0,0,0.08);
      text-align: center;
    }

    .stats {
      display: grid;
      grid-template-columns: repeat(auto-fit,minmax(200px,1fr));
      gap: 25px;
      margin-top: 50px;
    }

    .stat-box {
      background: linear-gradient(135deg,#fff,#eaf6ff);
      padding: 35px;
      border-radius: 24px;
    }

    .stat-box h3 {
      font-size: 42px;
      color: #0b5ed7;
      margin-bottom: 10px;
    }

    footer {
      background: #123c69;
      color: white;
      padding: 70px 8% 40px;
      margin-top: 80px;
    }

    .footer-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit,minmax(250px,1fr));
      gap: 40px;
    }

    footer h3 {
      margin-bottom: 18px;
      color: #fff;
    }

    footer p, footer li {
      color: #d6e3f3;
      line-height: 1.8;
      list-style: none;
    }

    .copyright {
      margin-top: 40px;
      text-align: center;
      border-top: 1px solid rgba(255,255,255,0.2);
      padding-top: 25px;
      color: #c9d8ea;
    }

    @media(max-width: 900px) {
      nav ul {
        display: none;
      }

      .hero {
        flex-direction: column;
        text-align: center;
      }

      .hero-text h1 {
        font-size: 48px;
      }

      .events {
        padding: 40px;
      }

      .pta-section {
        padding: 40px 25px;
      }
    }
  </style>
</head>
<body>

<header>
  <nav>
    <div class="logo">Smart <span>Tots</span></div>
    <ul>
      <li><a href="#home">Home</a></li>
      <li><a href="#about">About</a></li>
      <li><a href="#classes">Online Classes</a></li>
      <li><a href="#gallery">Gallery</a></li>
      <li><a href="#news">News</a></li>
      <li><a href="#events">Events</a></li>
      <li><a href="#pta">PTA</a></li>
      <li><a href="#contact">Contact</a></li>
    </ul>
  </nav>
</header>

<section class="hero" id="home">
  <div class="hero-text">
    <h1>Shaping Bright Futures at <span>Smart Tots</span></h1>
    <p>
      Welcome to Smart Tots Kindergarten & Junior School — a modern learning environment where children grow academically, creatively, spiritually, and socially through innovative education and digital learning.
    </p>

    <div class="hero-buttons">
      <a href="#classes" class="btn primary">Join Online Classes</a>
      <a href="#gallery" class="btn secondary">Explore Gallery</a>
    </div>
  </div>

  <div class="hero-image">
    <img src="https://images.unsplash.com/photo-1509062522246-3755977927d7?q=80&w=1200&auto=format&fit=crop" alt="School Kids">

    <div class="floating-card card1">
      <strong>500+</strong><br>
      Happy Learners
    </div>

    <div class="floating-card card2">
      <strong>Next Gen</strong><br>
      Digital Learning
    </div>
  </div>
</section>

<section id="about">
  <div class="section-title">
    <h2>Why Parents Choose Smart Tots</h2>
    <p>
      We combine technology, creativity, discipline, and excellence to provide a complete learning experience for every child.
    </p>
  </div>

  <div class="features">
    <div class="feature-box">
      <div class="feature-icon">🎓</div>
      <h3>Qualified Teachers</h3>
      <p>Professional and caring educators committed to nurturing every learner with excellence and passion.</p>
    </div>

    <div class="feature-box">
      <div class="feature-icon">💻</div>
      <h3>Online Learning</h3>
      <p>Interactive virtual classrooms, assignments, and digital learning tools for modern education.</p>
    </div>

    <div class="feature-box">
      <div class="feature-icon">⚽</div>
      <h3>Co-Curricular Activities</h3>
      <p>Sports, music, art, dance, and leadership programs that build confidence and creativity.</p>
    </div>

    <div class="feature-box">
      <div class="feature-icon">🚌</div>
      <h3>Safe Environment</h3>
      <p>A secure, child-friendly environment with modern facilities and caring staff members.</p>
    </div>
  </div>
</section>

<section id="classes">
  <div class="section-title">
    <h2>Smart Online Classes</h2>
    <p>
      Learning continues everywhere through our digital classroom platform.
    </p>
  </div>

  <div class="online-classes">
    <img src="https://images.unsplash.com/photo-1588072432836-e10032774350?q=80&w=1200&auto=format&fit=crop" alt="Online Learning">

    <div class="class-info">
      <h2 style="font-size:40px;color:#123c69;">Digital Learning Experience</h2>
      <p style="margin-top:20px;line-height:1.8;color:#555;">
        Our online classes allow learners to access lessons, assignments, live teaching sessions, and recorded content from anywhere.
      </p>

      <ul>
        <li>Live Zoom & Google Meet classes</li>
        <li>Homework & assignment portal</li>
        <li>Digital report cards</li>
        <li>Interactive learning videos</li>
        <li>Parent-teacher communication system</li>
      </ul>

      <a href="#contact" class="btn primary" style="margin-top:25px;">Register a Student</a>
    </div>
  </div>
</section>

<section id="gallery">
  <div class="section-title">
    <h2>School Gallery</h2>
    <p>
      Explore moments of learning, fun, sports, creativity, and memorable school activities.
    </p>
  </div>

  <div class="gallery">
    <img src="https://images.unsplash.com/photo-1503676260728-1c00da094a0b?q=80&w=1000&auto=format&fit=crop" alt="Gallery 1">
    <img src="https://images.unsplash.com/photo-1513258496099-48168024aec0?q=80&w=1000&auto=format&fit=crop" alt="Gallery 2">
    <img src="https://images.unsplash.com/photo-1509062522246-3755977927d7?q=80&w=1000&auto=format&fit=crop" alt="Gallery 3">
    <img src="https://images.unsplash.com/photo-1588072432904-843af37f03ed?q=80&w=1000&auto=format&fit=crop" alt="Gallery 4">
  </div>
</section>

<section id="news">
  <div class="section-title">
    <h2>Daily School News</h2>
    <p>
      Stay updated with announcements, student achievements, learning updates, and school programs.
    </p>
  </div>

  <div class="news-grid">
    <div class="news-card">
      <img src="https://images.unsplash.com/photo-1529390079861-591de354faf5?q=80&w=1200&auto=format&fit=crop" alt="News 1">
      <div class="news-content">
        <h3>Science Innovation Week</h3>
        <p>Students showcased amazing science projects and innovation ideas during the annual science exhibition.</p>
        <a href="#" class="btn secondary">Read More</a>
      </div>
    </div>

    <div class="news-card">
      <img src="https://images.unsplash.com/photo-1516321318423-f06f85e504b3?q=80&w=1200&auto=format&fit=crop" alt="News 2">
      <div class="news-content">
        <h3>Digital Learning Expansion</h3>
        <p>New smart classrooms and computer labs have been introduced to enhance technology-based learning.</p>
        <a href="#" class="btn secondary">Read More</a>
      </div>
    </div>

    <div class="news-card">
      <img src="https://images.unsplash.com/photo-1497486751825-1233686d5d80?q=80&w=1200&auto=format&fit=crop" alt="News 3">
      <div class="news-content">
        <h3>Sports Championship</h3>
        <p>Smart Tots students won multiple medals and trophies in the district junior sports competitions.</p>
        <a href="#" class="btn secondary">Read More</a>
      </div>
    </div>
  </div>
</section>

<section id="events">
  <div class="events">
    <div class="section-title" style="margin-bottom:20px;">
      <h2 style="color:white;">Upcoming School Events</h2>
      <p style="color:#e9f3ff;">Parents and learners can stay informed about all upcoming school activities and programs.</p>
    </div>

    <div class="event-list">
      <div class="event-item">
        <h4>📅 Parents Meeting</h4>
        <p>Quarterly PTA engagement and learner performance discussions.</p>
      </div>

      <div class="event-item">
        <h4>🎭 Talent Day</h4>
        <p>Music, dance, poetry, drama, and student creativity showcase.</p>
      </div>

      <div class="event-item">
        <h4>🏆 Sports Day</h4>
        <p>Exciting athletics and football competitions for all classes.</p>
      </div>

      <div class="event-item">
        <h4>🎓 Graduation Ceremony</h4>
        <p>Celebrating our top class learners as they transition to new levels.</p>
      </div>
    </div>
  </div>
</section>

<section id="pta">
  <div class="pta-section">
    <div class="section-title">
      <h2>Parents Teachers Association (PTA)</h2>
      <p>
        Building strong partnerships between parents and teachers to ensure academic excellence and student success.
      </p>
    </div>

    <div class="stats">
      <div class="stat-box">
        <h3>500+</h3>
        <p>Active Students</p>
      </div>

      <div class="stat-box">
        <h3>40+</h3>
        <p>Professional Teachers</p>
      </div>

      <div class="stat-box">
        <h3>15+</h3>
        <p>Learning Programs</p>
      </div>

      <div class="stat-box">
        <h3>98%</h3>
        <p>Parent Satisfaction</p>
      </div>
    </div>
  </div>
</section>

<footer id="contact">
  <div class="footer-grid">
    <div>
      <h3>Smart Tots Kindergarten & Junior</h3>
      <p>
        Empowering young minds through innovation, creativity, discipline, and modern learning experiences.
      </p>
    </div>

    <div>
      <h3>Quick Links</h3>
      <ul>
        <li>Admissions</li>
        <li>Online Classes</li>
        <li>School Gallery</li>
        <li>PTA Meetings</li>
        <li>School Calendar</li>
      </ul>
    </div>

    <div>
      <h3>Contact Us</h3>
      <p>Email: info@smarttots.edu</p>
      <p>Phone: +256 700 000000</p>
      <p>Ndese Kakakala, Mukono District, Uganda</p>
    </div>
  </div>

  <div class="copyright">
    © 2026 Smart Tots Kindergarten & Junior School. All Rights Reserved.
  </div>
  <section style="padding:80px 8%;background:#eef7ff;">
    <div class="section-title">
      <h2>Smart School Portal</h2>
      <p>Access digital learning tools, assignments, online streams, and school updates from anywhere.</p>
    </div>

    <div class="features">
      <div class="feature-box">
        <div class="feature-icon">📚</div>
        <h3>Student Portal</h3>
        <p>Students can access assignments, notes, recorded lessons, and exam results online.</p>
      </div>

      <div class="feature-box">
        <div class="feature-icon">🎥</div>
        <h3>Live Classes</h3>
        <p>Integrated live streaming and virtual classes for remote learning and revision sessions.</p>
      </div>

      <div class="feature-box">
        <div class="feature-icon">👩‍🏫</div>
        <h3>Teacher Dashboard</h3>
        <p>Teachers can upload assignments, manage attendance, and communicate with parents.</p>
      </div>

      <div class="feature-box">
        <div class="feature-icon">💬</div>
        <h3>WhatsApp Integration</h3>
        <p>Parents receive updates, reminders, and school communication directly on WhatsApp.</p>
      </div>
    </div>
  </section>

  <section style="padding:80px 8%;">
    <div class="section-title">
      <h2>Download Smart Tots App</h2>
      <p>Parents and students can access school services directly from their smartphones.</p>
    </div>

    <div style="background:linear-gradient(135deg,#0b5ed7,#00a6ff);padding:50px;border-radius:35px;text-align:center;color:white;">
      <h2 style="font-size:42px;margin-bottom:20px;">Smart Tots Mobile App</h2>
      <p style="max-width:700px;margin:auto;line-height:1.8;opacity:0.95;">
        Access online classes, school news, assignments, PTA updates, live streams, and announcements from your Android device.
      </p>

      <div style="margin-top:35px;display:flex;justify-content:center;gap:20px;flex-wrap:wrap;">
        <a href="#" class="btn" style="background:white;color:#0b5ed7;">Download APK</a>
        <a href="#contact" class="btn secondary" style="border-color:white;color:white;">Contact School</a>
      </div>
    </div>
  </section>

</footer>

  

<!-- CMS ADMIN PANEL -->
<section id="admin-login" style="padding:100px 8%;background:#0b1220;color:white;">
  <div style="max-width:450px;margin:auto;background:#1e293b;padding:40px;border-radius:30px;box-shadow:0 20px 40px rgba(0,0,0,0.3);">
    <h2 style="text-align:center;margin-bottom:15px;">Admin Login</h2>
    <p style="text-align:center;color:#cbd5e1;margin-bottom:30px;">Only authorized Smart Tots administrators can access the CMS dashboard.</p>

    <input type="text" id="adminUser" placeholder="Admin Username" style="width:100%;padding:16px;border:none;border-radius:15px;margin-bottom:18px;font-size:16px;">

    <input type="password" id="adminPass" placeholder="Admin Password" style="width:100%;padding:16px;border:none;border-radius:15px;margin-bottom:20px;font-size:16px;">

    <button onclick="adminLogin()" class="btn primary" style="width:100%;border:none;cursor:pointer;">Secure Login</button>

    <p id="loginMessage" style="margin-top:20px;text-align:center;color:#fca5a5;"></p>
  </div>
</section>

<section id="admin-panel" style="padding:100px 8%;background:#0f172a;color:white;display:none;"> style="padding:100px 8%;background:#0f172a;color:white;">
  <div class="section-title">
    <h2 style="color:white;">Smart Tots CMS Admin Panel</h2>
    <p style="color:#cbd5e1;">Manage website updates, upload photos, post news, and control school content live.</p>
  </div>

  <div style="display:grid;grid-template-columns:repeat(auto-fit,minmax(320px,1fr));gap:30px;">

    <div style="background:#1e293b;padding:30px;border-radius:25px;">
      <h3 style="margin-bottom:20px;">Upload School News</h3>
      <input type="text" id="newsTitle" placeholder="News Title" style="width:100%;padding:15px;border:none;border-radius:15px;margin-bottom:15px;">

      <textarea id="newsText" placeholder="News Details" style="width:100%;padding:15px;border:none;border-radius:15px;height:120px;margin-bottom:15px;"></textarea>

      <input type="text" id="newsImage" placeholder="Paste Image URL" style="width:100%;padding:15px;border:none;border-radius:15px;margin-bottom:15px;">

      <button onclick="uploadNews()" class="btn primary">Publish News</button>
    </div>

    <div style="background:#1e293b;padding:30px;border-radius:25px;">
      <h3 style="margin-bottom:20px;">Upload Gallery Photo</h3>

      <input type="text" id="galleryImage" placeholder="Paste Image URL" style="width:100%;padding:15px;border:none;border-radius:15px;margin-bottom:15px;">

      <button onclick="uploadGallery()" class="btn primary">Add Photo</button>
    </div>

    <div style="background:#1e293b;padding:30px;border-radius:25px;">
      <h3 style="margin-bottom:20px;">School Announcement</h3>

      <textarea id="announcement" placeholder="Write announcement" style="width:100%;padding:15px;border:none;border-radius:15px;height:140px;margin-bottom:15px;"></textarea>

      <button onclick="postAnnouncement()" class="btn primary">Post Announcement</button>

      <div id="announcementDisplay" style="margin-top:20px;background:#334155;padding:20px;border-radius:18px;"></div>
    </div>

  </div>
</section>

<script>

// ADMIN LOGIN SYSTEM
function adminLogin(){
  const username = document.getElementById('adminUser').value;
  const password = document.getElementById('adminPass').value;
  const loginMessage = document.getElementById('loginMessage');

  // Default Admin Credentials
  const adminUsername = 'admin';
  const adminPassword = 'smarttots123';

  if(username === adminUsername && password === adminPassword){
    document.getElementById('admin-panel').style.display = 'block';
    document.getElementById('admin-login').style.display = 'none';

    localStorage.setItem('adminLoggedIn', 'true');

    alert('Welcome to Smart Tots CMS Dashboard');
  } else {
    loginMessage.innerHTML = 'Invalid admin username or password';
  }
}

// Keep Admin Logged In
window.onload = function(){
  if(localStorage.getItem('adminLoggedIn') === 'true'){
    document.getElementById('admin-panel').style.display = 'block';
    document.getElementById('admin-login').style.display = 'none';
  }
}

// Upload News Function
function uploadNews(){
  const title = document.getElementById('newsTitle').value;
  const text = document.getElementById('newsText').value;
  const image = document.getElementById('newsImage').value;

  const newsContainer = document.querySelector('.news-grid');

  const card = document.createElement('div');
  card.classList.add('news-card');

  card.innerHTML = `
    <img src="${image}" alt="News">
    <div class="news-content">
      <h3>${title}</h3>
      <p>${text}</p>
      <a href="#" class="btn secondary">Read More</a>
    </div>
  `;

  newsContainer.prepend(card);

  alert('News published successfully');
}

// Upload Gallery Images
function uploadGallery(){
  const image = document.getElementById('galleryImage').value;

  const gallery = document.querySelector('.gallery');

  const img = document.createElement('img');
  img.src = image;

  gallery.prepend(img);

  alert('Gallery photo added successfully');
}

// Post Announcement
function postAnnouncement(){
  const announcement = document.getElementById('announcement').value;

  document.getElementById('announcementDisplay').innerHTML = announcement;

  alert('Announcement posted successfully');
}

// Smooth Navigation
const links = document.querySelectorAll('nav a');
links.forEach(link => {
  link.addEventListener('click', function(e){
    e.preventDefault();
    const target = document.querySelector(this.getAttribute('href'));
    target.scrollIntoView({behavior:'smooth'});
  });
});

// Dynamic News System
const newsContainer = document.querySelector('.news-grid');

const dynamicNews = [
  {
    title: 'Coding Club Launch',
    text: 'Smart Tots has launched a new coding and robotics club for learners.',
    image: 'https://images.unsplash.com/photo-1516321318423-f06f85e504b3?q=80&w=1200&auto=format&fit=crop'
  },
  {
    title: 'Online Learning Upgrade',
    text: 'Parents can now monitor assignments and student progress online.',
    image: 'https://images.unsplash.com/photo-1588072432904-843af37f03ed?q=80&w=1200&auto=format&fit=crop'
  }
];

setTimeout(() => {
  dynamicNews.forEach(news => {
    const card = document.createElement('div');
    card.classList.add('news-card');

    card.innerHTML = `
      <img src="${news.image}" alt="News">
      <div class="news-content">
        <h3>${news.title}</h3>
        <p>${news.text}</p>
        <a href="#" class="btn secondary">Read More</a>
      </div>
    `;

    newsContainer.appendChild(card);
  });
}, 2000);

// PTA Registration Popup
function registerPTA() {
  const parentName = prompt('Enter Parent Name');

  if(parentName){
    alert(parentName + ' successfully registered for PTA updates.');
    localStorage.setItem('ptaParent', parentName);
  }
}

// Student Registration Form
function registerStudent(){
  const student = prompt('Enter Student Name');

  if(student){
    alert(student + ' registered successfully at Smart Tots.');
    localStorage.setItem('studentName', student);
  }
}

// Live Clock
const footer = document.querySelector('.copyright');

setInterval(() => {
  const now = new Date();
  footer.innerHTML = `© 2026 Smart Tots Kindergarten & Junior School | ${now.toLocaleTimeString()}`;
},1000);

// Online Class Button Actions
const onlineButtons = document.querySelectorAll('.primary');

onlineButtons.forEach(btn => {
  btn.addEventListener('click', () => {
    console.log('Opening Online Class Portal');
  });
});

</script>

</body>
</html>

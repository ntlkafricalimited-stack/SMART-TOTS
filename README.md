```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>SMART TOTS Kindergarten</title>

  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700&display=swap" rel="stylesheet">

  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    html {
      scroll-behavior: smooth;
    }

    body {
      font-family: 'Poppins', sans-serif;
      background: #f8fafc;
      color: #0f172a;
      overflow-x: hidden;
    }

    nav {
      position: fixed;
      top: 0;
      width: 100%;
      background: rgba(15, 23, 42, 0.85);
      backdrop-filter: blur(10px);
      padding: 18px 8%;
      display: flex;
      justify-content: space-between;
      align-items: center;
      z-index: 1000;
    }

    nav h2 {
      color: white;
      font-size: 28px;
    }

    nav ul {
      display: flex;
      gap: 25px;
      list-style: none;
    }

    nav ul li a {
      text-decoration: none;
      color: white;
      font-weight: 500;
      transition: 0.3s;
    }

    nav ul li a:hover {
      color: #06b6d4;
    }

    .hero {
      height: 100vh;
      background: linear-gradient(rgba(0,0,0,0.5), rgba(0,0,0,0.5)),
      url('https://images.unsplash.com/photo-1509062522246-3755977927d7?q=80&w=1200&auto=format&fit=crop') center/cover;
      display: flex;
      justify-content: center;
      align-items: center;
      text-align: center;
      color: white;
      padding: 20px;
    }

    .hero-content h1 {
      font-size: 60px;
      margin-bottom: 20px;
    }

    .hero-content p {
      font-size: 20px;
      margin-bottom: 30px;
    }

    .btn {
      display: inline-block;
      padding: 14px 30px;
      background: #4f46e5;
      color: white;
      border-radius: 50px;
      text-decoration: none;
      margin: 10px;
      transition: 0.3s;
    }

    .btn:hover {
      background: #06b6d4;
      transform: translateY(-5px);
    }

    section {
      padding: 80px 8%;
    }

    .section-title {
      text-align: center;
      margin-bottom: 50px;
    }

    .section-title h2 {
      font-size: 40px;
      color: #4f46e5;
    }

    .about {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
      gap: 40px;
      align-items: center;
    }

    .about img {
      width: 100%;
      border-radius: 20px;
    }

    .cards {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
      gap: 25px;
    }

    .card {
      background: white;
      padding: 30px;
      border-radius: 20px;
      box-shadow: 0 10px 25px rgba(0,0,0,0.08);
      transition: 0.4s;
      text-align: center;
    }

    .card:hover {
      transform: translateY(-10px);
    }

    .card h3 {
      margin: 15px 0;
      color: #4f46e5;
    }

    .gallery {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
      gap: 20px;
    }

    .gallery img {
      width: 100%;
      height: 250px;
      object-fit: cover;
      border-radius: 20px;
      transition: 0.4s;
    }

    .gallery img:hover {
      transform: scale(1.05);
    }

    .contact {
      background: #0f172a;
      color: white;
      border-radius: 25px;
      padding: 50px;
      text-align: center;
    }

    .contact p {
      margin: 15px 0;
    }

    footer {
      text-align: center;
      padding: 25px;
      background: #020617;
      color: white;
    }

    @media(max-width:768px){
      nav {
        flex-direction: column;
        gap: 15px;
      }

      .hero-content h1 {
        font-size: 38px;
      }

      .hero-content p {
        font-size: 16px;
      }

      section {
        padding: 60px 5%;
      }
    }
  </style>
</head>
<body>

  <nav>
    <h2>SMART TOTS</h2>

    <ul>
      <li><a href="#home">Home</a></li>
      <li><a href="#about">About</a></li>
      <li><a href="#programs">Programs</a></li>
      <li><a href="#gallery">Gallery</a></li>
      <li><a href="#contact">Contact</a></li>
    </ul>
  </nav>

  <section class="hero" id="home">
    <div class="hero-content">
      <h1>Shaping Future Leaders</h1>
      <p>Modern Christian Kindergarten with Smart Learning Environment</p>

      <a href="#contact" class="btn">Enroll Now</a>
      <a href="#programs" class="btn">Explore Programs</a>
    </div>
  </section>

  <section id="about">
    <div class="section-title">
      <h2>About Us</h2>
    </div>

    <div class="about">
      <img src="https://images.unsplash.com/photo-1516627145497-ae6968895b74?q=80&w=1200&auto=format&fit=crop">

      <div>
        <h2>SMART TOTS Kindergarten</h2>
        <br>
        <p>
          We provide a safe, creative and modern learning environment where children grow academically, spiritually and socially.
        </p>
        <br>
        <p>
          Our programs combine digital learning, Christian values and practical creativity to shape tomorrow’s leaders.
        </p>
      </div>
    </div>
  </section>

  <section id="programs">
    <div class="section-title">
      <h2>Our Programs</h2>
    </div>

    <div class="cards">
      <div class="card">
        <h3>Baby Class</h3>
        <p>Early childhood development and creative play.</p>
      </div>

      <div class="card">
        <h3>Middle Class</h3>
        <p>Interactive learning with smart activities.</p>
      </div>

      <div class="card">
        <h3>Top Class</h3>
        <p>Preparing children for primary education success.</p>
      </div>

      <div class="card">
        <h3>Daycare</h3>
        <p>Safe and nurturing daycare services for children.</p>
      </div>
    </div>
  </section>

  <section id="gallery">
    <div class="section-title">
      <h2>Gallery</h2>
    </div>

    <div class="gallery">
      <img src="https://images.unsplash.com/photo-1503454537195-1dcabb73ffb9?q=80&w=1200&auto=format&fit=crop">

      <img src="https://images.unsplash.com/photo-1516627145497-ae6968895b74?q=80&w=1200&auto=format&fit=crop">

      <img src="https://images.unsplash.com/photo-1542816417-0983670d17e1?q=80&w=1200&auto=format&fit=crop">

      <img src="https://images.unsplash.com/photo-1509062522246-3755977927d7?q=80&w=1200&auto=format&fit=crop">
    </div>
  </section>

  <section id="contact">
    <div class="contact">
      <h2>Contact Us</h2>

      <p>Email: smarttots@gmail.com</p>
      <p>Phone: +256 XXX XXX XXX</p>
      <p>Kampala, Uganda</p>

      <a href="https://wa.me/256700000000" class="btn">WhatsApp Us</a>
    </div>
  </section>

  <footer>
    <p>© 2026 SMART TOTS Kindergarten. All Rights Reserved.</p>
  </footer>

</body>
</html>
```

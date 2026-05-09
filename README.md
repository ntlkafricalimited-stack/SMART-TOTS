<html lang="en" class="scroll-smooth">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <meta name="description" content="Smart Tots Junior — Premium Tech-Focused Junior Academy in Mukono, Uganda. Coding, Robotics, AI & STEM Education for children ages 3–9."/>
  <meta name="keywords" content="Smart Tots Junior, coding for kids Uganda, robotics school, STEM academy Mukono, tech school for children"/>
  <meta name="author" content="Smart Tots Junior"/>

  <title>Smart Tots Junior | Nurturing Tomorrow’s Tech Geniuses</title>

  <!-- Tailwind -->
  <script src="https://cdn.tailwindcss.com"></script>

  <!-- Icons -->
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.2/css/all.min.css"/>

  <!-- Fonts -->
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link href="https://fonts.googleapis.com/css2?family=Space+Grotesk:wght@300;400;500;600;700&display=swap" rel="stylesheet">

  <style>
    :root{
      --bg:#050816;
      --card:#0f172a;
      --text:#f8fafc;
      --muted:#94a3b8;
      --primary:#00d9ff;
      --secondary:#7c3aed;
      --accent:#22c55e;
      --orange:#fb923c;
    }

    body.light{
      --bg:#f8fafc;
      --card:#ffffff;
      --text:#0f172a;
      --muted:#475569;
    }

    *{
      font-family: 'Space Grotesk', sans-serif;
    }

    body{
      background: var(--bg);
      color: var(--text);
      transition: all .4s ease;
      overflow-x: hidden;
    }

    .glass{
      background: rgba(255,255,255,0.06);
      backdrop-filter: blur(14px);
      border: 1px solid rgba(255,255,255,0.08);
    }

    .gradient-text{
      background: linear-gradient(90deg,#00d9ff,#7c3aed,#22c55e,#fb923c);
      -webkit-background-clip:text;
      -webkit-text-fill-color:transparent;
    }

    .hero-bg{
      background:
      linear-gradient(to bottom right, rgba(2,6,23,.85), rgba(15,23,42,.6)),
      url('https://images.unsplash.com/photo-1588072432904-843af37f03ed?q=80&w=1600&auto=format&fit=crop');
      background-size: cover;
      background-position: center;
      background-attachment: fixed;
    }

    .glow{
      box-shadow: 0 0 30px rgba(0,217,255,.35);
    }

    .card-hover{
      transition: all .4s ease;
    }

    .card-hover:hover{
      transform: translateY(-10px);
      box-shadow: 0 20px 60px rgba(0,0,0,.35);
    }

    .nav-scrolled{
      background: rgba(2,6,23,.9);
      backdrop-filter: blur(12px);
      box-shadow: 0 10px 30px rgba(0,0,0,.2);
    }

    .fade-up{
      opacity:0;
      transform:translateY(40px);
      transition: all 1s ease;
    }

    .fade-up.show{
      opacity:1;
      transform:translateY(0);
    }

    .gallery img{
      transition: all .5s ease;
    }

    .gallery img:hover{
      transform: scale(1.05);
    }

    .floating{
      animation: float 5s ease-in-out infinite;
    }

    @keyframes float{
      0%,100%{transform: translateY(0px);}
      50%{transform: translateY(-15px);}
    }

    .blob{
      position:absolute;
      width:400px;
      height:400px;
      border-radius:999px;
      filter: blur(90px);
      opacity:.18;
      z-index:-1;
    }

    .blob1{
      background:#00d9ff;
      top:-100px;
      left:-100px;
    }

    .blob2{
      background:#7c3aed;
      right:-120px;
      top:300px;
    }

    .blob3{
      background:#22c55e;
      bottom:-100px;
      left:30%;
    }

    .mobile-menu{
      max-height:0;
      overflow:hidden;
      transition:max-height .4s ease;
    }

    .mobile-menu.active{
      max-height:500px;
    }

    input, textarea{
      background: rgba(255,255,255,.04);
      border:1px solid rgba(255,255,255,.08);
    }

    .gradient-btn{
      background: linear-gradient(135deg,#00d9ff,#7c3aed);
    }

    .gradient-btn:hover{
      transform: scale(1.03);
      box-shadow: 0 10px 35px rgba(0,217,255,.35);
    }

    ::selection{
      background:#00d9ff;
      color:#000;
    }
  </style>
</head>

<body>

  <!-- Decorative Blobs -->
  <div class="blob blob1"></div>
  <div class="blob blob2"></div>
  <div class="blob blob3"></div>

  <!-- NAVBAR -->
  <header id="navbar" class="fixed w-full top-0 z-50 transition-all duration-500">
    <div class="max-w-7xl mx-auto px-6 py-4 flex items-center justify-between">

      <div class="flex items-center gap-3">
        <div class="w-11 h-11 rounded-2xl bg-gradient-to-r from-cyan-400 to-purple-600 flex items-center justify-center text-white font-bold text-xl">
          ST
        </div>
        <div>
          <h1 class="font-bold text-lg">Smart Tots Junior</h1>
          <p class="text-xs text-slate-400">Tech Academy</p>
        </div>
      </div>

      <!-- Desktop Menu -->
      <nav class="hidden md:flex items-center gap-8">
        <a href="#about" class="hover:text-cyan-400 transition">About</a>
        <a href="#programs" class="hover:text-cyan-400 transition">Programs</a>
        <a href="#gallery" class="hover:text-cyan-400 transition">Gallery</a>
        <a href="#admissions" class="hover:text-cyan-400 transition">Admissions</a>
        <a href="#contact" class="hover:text-cyan-400 transition">Contact</a>

        <button id="themeToggle" class="w-10 h-10 rounded-full glass">
          <i class="fa-solid fa-moon"></i>
        </button>

        <a href="#contact" class="px-5 py-3 rounded-full gradient-btn text-white font-semibold transition-all">
          Join Now
        </a>
      </nav>

      <!-- Mobile -->
      <div class="flex items-center gap-3 md:hidden">
        <button id="themeToggleMobile" class="w-10 h-10 rounded-full glass">
          <i class="fa-solid fa-moon"></i>
        </button>

        <button id="menuBtn" class="text-2xl">
          <i class="fa-solid fa-bars"></i>
        </button>
      </div>
    </div>

    <!-- Mobile Menu -->
    <div id="mobileMenu" class="mobile-menu md:hidden glass">
      <div class="flex flex-col px-6 py-6 gap-5">
        <a href="#about">About</a>
        <a href="#programs">Programs</a>
        <a href="#gallery">Gallery</a>
        <a href="#admissions">Admissions</a>
        <a href="#contact">Contact</a>

        <a href="#contact" class="gradient-btn text-center py-3 rounded-full font-semibold">
          Join Now
        </a>
      </div>
    </div>
  </header>

  <!-- HERO -->
  <section class="hero-bg min-h-screen flex items-center relative overflow-hidden">
    <div class="max-w-7xl mx-auto px-6 py-32 grid lg:grid-cols-2 gap-16 items-center">

      <div class="fade-up">
        <span class="inline-block px-4 py-2 rounded-full glass text-sm mb-6">
          Future-Ready Learning Environment
        </span>

        <h1 class="text-5xl md:text-7xl font-bold leading-tight mb-6">
          Nurturing
          <span class="gradient-text">
            Tomorrow’s
          </span>
          Tech Geniuses
        </h1>

        <p class="text-lg md:text-xl text-slate-300 leading-relaxed mb-10 max-w-2xl">
          Smart Tots Junior is a next-generation junior academy in Mukono, Uganda empowering children ages 3–9 with coding, robotics, AI basics, STEM creativity, and holistic development.
        </p>

        <div class="flex flex-wrap gap-4">
          <a href="#admissions" class="px-8 py-4 rounded-full gradient-btn text-white font-semibold transition-all">
            Enroll Today
          </a>

          <a href="#" class="px-8 py-4 rounded-full glass hover:scale-105 transition flex items-center gap-3">
            <i class="fa-solid fa-play"></i>
            Watch Video
          </a>
        </div>

        <div class="flex gap-10 mt-14">
          <div>
            <h3 class="text-3xl font-bold gradient-text">500+</h3>
            <p class="text-slate-400">Young Learners</p>
          </div>

          <div>
            <h3 class="text-3xl font-bold gradient-text">20+</h3>
            <p class="text-slate-400">STEM Programs</p>
          </div>

          <div>
            <h3 class="text-3xl font-bold gradient-text">98%</h3>
            <p class="text-slate-400">Parent Satisfaction</p>
          </div>
        </div>
      </div>

      <div class="relative fade-up floating">
        <img
          src="https://images.unsplash.com/photo-1509062522246-3755977927d7?q=80&w=1200&auto=format&fit=crop"
          class="rounded-[40px] shadow-2xl glow"
          alt="Kids learning technology"
        />
      </div>
    </div>
  </section>

  <!-- ABOUT -->
  <section id="about" class="py-28">
    <div class="max-w-7xl mx-auto px-6 grid lg:grid-cols-2 gap-16 items-center">

      <div class="fade-up">
        <img
          src="https://images.unsplash.com/photo-1516321318423-f06f85e504b3?q=80&w=1200&auto=format&fit=crop"
          class="rounded-[35px]"
          alt="Smart classroom"
        />
      </div>

      <div class="fade-up">
        <span class="text-cyan-400 font-semibold uppercase tracking-widest">
          About Smart Tots
        </span>

        <h2 class="text-4xl md:text-5xl font-bold mt-4 mb-8">
          Building Brilliant Young Minds Through Technology
        </h2>

        <p class="text-slate-400 leading-relaxed mb-6">
          Smart Tots Junior is a premium early childhood academy designed to prepare children for the future through immersive tech education and holistic learning experiences.
        </p>

        <p class="text-slate-400 leading-relaxed mb-8">
          Located in Ndese Kakakala, Mukono District, Uganda, we combine creativity, innovation, robotics, coding, AI exploration, STEM activities, and emotional development in a safe and inspiring environment.
        </p>

        <div class="grid sm:grid-cols-2 gap-5">
          <div class="glass p-6 rounded-3xl">
            <i class="fa-solid fa-bullseye text-cyan-400 text-2xl mb-4"></i>
            <h3 class="font-bold text-xl mb-2">Our Mission</h3>
            <p class="text-slate-400 text-sm">
              Empower children with future-ready skills and creativity.
            </p>
          </div>

          <div class="glass p-6 rounded-3xl">
            <i class="fa-solid fa-eye text-purple-400 text-2xl mb-4"></i>
            <h3 class="font-bold text-xl mb-2">Our Vision</h3>
            <p class="text-slate-400 text-sm">
              Become Africa’s leading tech-focused junior academy.
            </p>
          </div>
        </div>
      </div>
    </div>
  </section>

  <!-- PROGRAMS -->
  <section id="programs" class="py-28 bg-black/10">
    <div class="max-w-7xl mx-auto px-6">

      <div class="text-center max-w-3xl mx-auto fade-up">
        <span class="text-cyan-400 uppercase tracking-widest font-semibold">
          Our Programs
        </span>

        <h2 class="text-4xl md:text-5xl font-bold mt-4 mb-6">
          Future-Focused Learning Tracks
        </h2>

        <p class="text-slate-400">
          Carefully crafted learning journeys for every stage of your child’s growth.
        </p>
      </div>

      <div class="grid md:grid-cols-3 gap-8 mt-16">

        <div class="glass rounded-[35px] p-8 card-hover fade-up">
          <div class="w-16 h-16 rounded-2xl bg-cyan-500/20 flex items-center justify-center text-cyan-400 text-2xl mb-6">
            <i class="fa-solid fa-puzzle-piece"></i>
          </div>

          <h3 class="text-2xl font-bold mb-4">Tiny Coders</h3>
          <p class="text-slate-400 mb-5">
            Ages 3–5
          </p>

          <ul class="space-y-3 text-slate-300">
            <li>• Coding through games</li>
            <li>• Creative storytelling</li>
            <li>• STEM play activities</li>
            <li>• Digital creativity</li>
          </ul>
        </div>

        <div class="glass rounded-[35px] p-8 card-hover fade-up">
          <div class="w-16 h-16 rounded-2xl bg-purple-500/20 flex items-center justify-center text-purple-400 text-2xl mb-6">
            <i class="fa-solid fa-robot"></i>
          </div>

          <h3 class="text-2xl font-bold mb-4">Tech Explorers</h3>
          <p class="text-slate-400 mb-5">
            Ages 6–7
          </p>

          <ul class="space-y-3 text-slate-300">
            <li>• Robotics basics</li>
            <li>• Scratch coding</li>
            <li>• AI awareness</li>
            <li>• Creative problem solving</li>
          </ul>
        </div>

        <div class="glass rounded-[35px] p-8 card-hover fade-up">
          <div class="w-16 h-16 rounded-2xl bg-green-500/20 flex items-center justify-center text-green-400 text-2xl mb-6">
            <i class="fa-solid fa-microchip"></i>
          </div>

          <h3 class="text-2xl font-bold mb-4">Future Innovators</h3>
          <p class="text-slate-400 mb-5">
            Ages 8–9
          </p>

          <ul class="space-y-3 text-slate-300">
            <li>• Beginner AI concepts</li>
            <li>• Robotics projects</li>
            <li>• STEM innovation labs</li>
            <li>• Leadership development</li>
          </ul>
        </div>

      </div>
    </div>
  </section>

  <!-- WHY -->
  <section class="py-28">
    <div class="max-w-7xl mx-auto px-6">

      <div class="text-center max-w-3xl mx-auto fade-up">
        <span class="text-cyan-400 uppercase tracking-widest font-semibold">
          Why Smart Tots
        </span>

        <h2 class="text-4xl md:text-5xl font-bold mt-4 mb-6">
          A New Standard for Early Learning
        </h2>
      </div>

      <div class="grid md:grid-cols-2 lg:grid-cols-4 gap-8 mt-16">

        <div class="glass p-8 rounded-[30px] text-center card-hover fade-up">
          <i class="fa-solid fa-user-group text-cyan-400 text-4xl mb-5"></i>
          <h3 class="font-bold text-xl mb-3">Small Classes</h3>
          <p class="text-slate-400">
            Personalized learning and close mentorship.
          </p>
        </div>

        <div class="glass p-8 rounded-[30px] text-center card-hover fade-up">
          <i class="fa-solid fa-laptop-code text-purple-400 text-4xl mb-5"></i>
          <h3 class="font-bold text-xl mb-3">Latest Tech</h3>
          <p class="text-slate-400">
            Robotics kits, coding labs, and AI tools.
          </p>
        </div>

        <div class="glass p-8 rounded-[30px] text-center card-hover fade-up">
          <i class="fa-solid fa-graduation-cap text-green-400 text-4xl mb-5"></i>
          <h3 class="font-bold text-xl mb-3">Expert Facilitators</h3>
          <p class="text-slate-400">
            Passionate educators trained in modern STEM education.
          </p>
        </div>

        <div class="glass p-8 rounded-[30px] text-center card-hover fade-up">
          <i class="fa-solid fa-shield-heart text-orange-400 text-4xl mb-5"></i>
          <h3 class="font-bold text-xl mb-3">Safe Environment</h3>
          <p class="text-slate-400">
            Secure, nurturing, and child-friendly learning spaces.
          </p>
        </div>

      </div>
    </div>
  </section>

  <!-- FACILITIES -->
  <section class="py-28 bg-black/10">
    <div class="max-w-7xl mx-auto px-6">

      <div class="grid lg:grid-cols-2 gap-16 items-center">

        <div class="fade-up">
          <span class="text-cyan-400 uppercase tracking-widest font-semibold">
            Facilities & Technology
          </span>

          <h2 class="text-4xl md:text-5xl font-bold mt-4 mb-8">
            Inspiring Spaces for Creative Discovery
          </h2>

          <div class="space-y-6">

            <div class="glass p-6 rounded-3xl">
              <h3 class="font-bold text-xl mb-2">Robotics & AI Labs</h3>
              <p class="text-slate-400">
                Interactive learning using modern robotics kits and beginner AI tools.
              </p>
            </div>

            <div class="glass p-6 rounded-3xl">
              <h3 class="font-bold text-xl mb-2">Creative Media Studio</h3>
              <p class="text-slate-400">
                Digital storytelling, animation, and visual creativity for children.
              </p>
            </div>

            <div class="glass p-6 rounded-3xl">
              <h3 class="font-bold text-xl mb-2">Outdoor Play & Innovation Area</h3>
              <p class="text-slate-400">
                Healthy balance of active play, teamwork, and exploration.
              </p>
            </div>

          </div>
        </div>

        <div class="fade-up">
          <img
            src="https://images.unsplash.com/photo-1503676260728-1c00da094a0b?q=80&w=1200&auto=format&fit=crop"
            class="rounded-[40px]"
            alt="Modern classroom"
          />
        </div>

      </div>
    </div>
  </section>

  <!-- GALLERY -->
  <section id="gallery" class="py-28">
    <div class="max-w-7xl mx-auto px-6">

      <div class="text-center fade-up">
        <span class="text-cyan-400 uppercase tracking-widest font-semibold">
          Gallery
        </span>

        <h2 class="text-4xl md:text-5xl font-bold mt-4 mb-6">
          Moments of Innovation
        </h2>
      </div>

      <div class="gallery grid md:grid-cols-2 lg:grid-cols-3 gap-6 mt-16">

        <img src="https://images.unsplash.com/photo-1513258496099-48168024aec0?q=80&w=1200&auto=format&fit=crop" class="rounded-[30px] h-80 w-full object-cover fade-up"/>

        <img src="https://images.unsplash.com/photo-1509062522246-3755977927d7?q=80&w=1200&auto=format&fit=crop" class="rounded-[30px] h-80 w-full object-cover fade-up"/>

        <img src="https://images.unsplash.com/photo-1516321497487-e288fb19713f?q=80&w=1200&auto=format&fit=crop" class="rounded-[30px] h-80 w-full object-cover fade-up"/>

        <img src="https://images.unsplash.com/photo-1517486808906-6ca8b3f04846?q=80&w=1200&auto=format&fit=crop" class="rounded-[30px] h-80 w-full object-cover fade-up"/>

        <img src="https://images.unsplash.com/photo-1503454537195-1dcabb73ffb9?q=80&w=1200&auto=format&fit=crop" class="rounded-[30px] h-80 w-full object-cover fade-up"/>

        <img src="https://images.unsplash.com/photo-1497486751825-1233686d5d80?q=80&w=1200&auto=format&fit=crop" class="rounded-[30px] h-80 w-full object-cover fade-up"/>

      </div>
    </div>
  </section>

  <!-- TESTIMONIALS -->
  <section class="py-28 bg-black/10">
    <div class="max-w-7xl mx-auto px-6">

      <div class="text-center fade-up">
        <span class="text-cyan-400 uppercase tracking-widest font-semibold">
          Testimonials
        </span>

        <h2 class="text-4xl md:text-5xl font-bold mt-4 mb-6">
          What Parents Say
        </h2>
      </div>

      <div class="grid md:grid-cols-3 gap-8 mt-16">

        <div class="glass p-8 rounded-[35px] fade-up">
          <p class="text-slate-300 leading-relaxed mb-6">
            “Smart Tots transformed my child’s confidence and creativity. The robotics classes are amazing.”
          </p>

          <div class="flex items-center gap-4">
            <div class="w-14 h-14 rounded-full bg-cyan-500"></div>
            <div>
              <h4 class="font-bold">Sarah N.</h4>
              <p class="text-slate-400 text-sm">Parent</p>
            </div>
          </div>
        </div>

        <div class="glass p-8 rounded-[35px] fade-up">
          <p class="text-slate-300 leading-relaxed mb-6">
            “The best early learning environment we’ve experienced in Uganda.”
          </p>

          <div class="flex items-center gap-4">
            <div class="w-14 h-14 rounded-full bg-purple-500"></div>
            <div>
              <h4 class="font-bold">Michael K.</h4>
              <p class="text-slate-400 text-sm">Parent</p>
            </div>
          </div>
        </div>

        <div class="glass p-8 rounded-[35px] fade-up">
          <p class="text-slate-300 leading-relaxed mb-6">
            “I love coding games and building robots with my friends!”
          </p>

          <div class="flex items-center gap-4">
            <div class="w-14 h-14 rounded-full bg-green-500"></div>
            <div>
              <h4 class="font-bold">Daniel, Age 8</h4>
              <p class="text-slate-400 text-sm">Student</p>
            </div>
          </div>
        </div>

      </div>
    </div>
  </section>

  <!-- ADMISSIONS -->
  <section id="admissions" class="py-28">
    <div class="max-w-6xl mx-auto px-6">

      <div class="glass rounded-[45px] p-10 md:p-16 text-center fade-up">

        <span class="text-cyan-400 uppercase tracking-widest font-semibold">
          Admissions
        </span>

        <h2 class="text-4xl md:text-6xl font-bold mt-4 mb-6">
          Begin Your Child’s Future Today
        </h2>

        <p class="text-slate-400 max-w-3xl mx-auto leading-relaxed mb-12">
          Our admissions process is simple and designed to help every child find the perfect learning path.
        </p>

        <div class="grid md:grid-cols-3 gap-8 text-left mb-12">

          <div class="glass rounded-3xl p-6">
            <h3 class="font-bold text-xl mb-3">1. Inquiry</h3>
            <p class="text-slate-400">
              Reach out to our admissions team or visit our campus.
            </p>
          </div>

          <div class="glass rounded-3xl p-6">
            <h3 class="font-bold text-xl mb-3">2. Assessment</h3>
            <p class="text-slate-400">
              Friendly child interaction and placement guidance.
            </p>
          </div>

          <div class="glass rounded-3xl p-6">
            <h3 class="font-bold text-xl mb-3">3. Enrollment</h3>
            <p class="text-slate-400">
              Complete registration and join the Smart Tots family.
            </p>
          </div>

        </div>

        <div class="flex flex-wrap justify-center gap-5">
          <a href="#contact" class="gradient-btn px-10 py-4 rounded-full font-semibold text-white transition-all">
            Apply Now
          </a>

          <div class="glass px-8 py-4 rounded-full">
            Tuition Packages Available
          </div>
        </div>

      </div>
    </div>
  </section>

  <!-- CONTACT -->
  <section id="contact" class="py-28 bg-black/10">
    <div class="max-w-7xl mx-auto px-6">

      <div class="grid lg:grid-cols-2 gap-14">

        <div class="fade-up">
          <span class="text-cyan-400 uppercase tracking-widest font-semibold">
            Contact Us
          </span>

          <h2 class="text-4xl md:text-5xl font-bold mt-4 mb-8">
            Let’s Build Your Child’s Future
          </h2>

          <div class="space-y-6 mb-10">

            <div class="flex gap-4 items-start">
              <i class="fa-solid fa-location-dot text-cyan-400 text-xl mt-1"></i>
              <div>
                <h4 class="font-bold">Location</h4>
                <p class="text-slate-400">
                  Ndese Kakakala, Mukono District, Uganda
                </p>
              </div>
            </div>

            <div class="flex gap-4 items-start">
              <i class="fa-solid fa-phone text-purple-400 text-xl mt-1"></i>
              <div>
                <h4 class="font-bold">Phone</h4>
                <p class="text-slate-400">
                  +256 700 000000
                </p>
              </div>
            </div>

            <div class="flex gap-4 items-start">
              <i class="fa-solid fa-envelope text-green-400 text-xl mt-1"></i>
              <div>
                <h4 class="font-bold">Email</h4>
                <p class="text-slate-400">
                  info@smarttotsjunior.com
                </p>
              </div>
            </div>

          </div>

          <!-- MAP -->
          <div class="rounded-[35px] overflow-hidden h-80">
            <iframe
              class="w-full h-full"
              src="https://maps.google.com/maps?q=Mukono%20Uganda&t=&z=13&ie=UTF8&iwloc=&output=embed"
              loading="lazy">
            </iframe>
          </div>
        </div>

        <!-- FORM -->
        <div class="glass rounded-[40px] p-8 md:p-10 fade-up">

          <form id="contactForm" class="space-y-6">

            <div>
              <label class="block mb-2">Parent Name</label>
              <input type="text" id="name" required class="w-full px-5 py-4 rounded-2xl outline-none"/>
            </div>

            <div>
              <label class="block mb-2">Email Address</label>
              <input type="email" id="email" required class="w-full px-5 py-4 rounded-2xl outline-none"/>
            </div>

            <div>
              <label class="block mb-2">Phone Number</label>
              <input type="tel" id="phone" required class="w-full px-5 py-4 rounded-2xl outline-none"/>
            </div>

            <div>
              <label class="block mb-2">Message</label>
              <textarea id="message" rows="5" required class="w-full px-5 py-4 rounded-2xl outline-none"></textarea>
            </div>

            <button type="submit" class="gradient-btn w-full py-4 rounded-2xl font-semibold text-white transition-all">
              Send Inquiry
            </button>

            <p id="formMessage" class="text-sm"></p>

          </form>

        </div>

      </div>
    </div>
  </section>

  <!-- FOOTER -->
  <footer class="py-12 border-t border-white/10">
    <div class="max-w-7xl mx-auto px-6">

      <div class="grid md:grid-cols-4 gap-10">

        <div>
          <h3 class="text-2xl font-bold gradient-text mb-4">
            Smart Tots Junior
          </h3>

          <p class="text-slate-400 leading-relaxed">
            Premium tech-focused junior academy preparing the next generation of innovators.
          </p>
        </div>

        <div>
          <h4 class="font-bold mb-4">Quick Links</h4>
          <ul class="space-y-3 text-slate-400">
            <li><a href="#about">About</a></li>
            <li><a href="#programs">Programs</a></li>
            <li><a href="#gallery">Gallery</a></li>
            <li><a href="#contact">Contact</a></li>
          </ul>
        </div>

        <div>
          <h4 class="font-bold mb-4">Programs</h4>
          <ul class="space-y-3 text-slate-400">
            <li>Tiny Coders</li>
            <li>Tech Explorers</li>
            <li>Future Innovators</li>
          </ul>
        </div>

        <div>
          <h4 class="font-bold mb-4">Follow Us</h4>

          <div class="flex gap-4 text-xl">
            <a href="#" class="w-12 h-12 rounded-full glass flex items-center justify-center hover:scale-110 transition">
              <i class="fab fa-facebook-f"></i>
            </a>

            <a href="#" class="w-12 h-12 rounded-full glass flex items-center justify-center hover:scale-110 transition">
              <i class="fab fa-instagram"></i>
            </a>

            <a href="#" class="w-12 h-12 rounded-full glass flex items-center justify-center hover:scale-110 transition">
              <i class="fab fa-youtube"></i>
            </a>

            <a href="#" class="w-12 h-12 rounded-full glass flex items-center justify-center hover:scale-110 transition">
              <i class="fab fa-tiktok"></i>
            </a>
          </div>
        </div>

      </div>

      <div class="border-t border-white/10 mt-12 pt-8 text-center text-slate-500">
        © 2026 Smart Tots Junior. All rights reserved.
      </div>

    </div>
  </footer>

  <!-- JAVASCRIPT -->
  <script>

    // NAVBAR SCROLL
    const navbar = document.getElementById('navbar');

    window.addEventListener('scroll', () => {
      if(window.scrollY > 50){
        navbar.classList.add('nav-scrolled');
      }else{
        navbar.classList.remove('nav-scrolled');
      }
    });

    // MOBILE MENU
    const menuBtn = document.getElementById('menuBtn');
    const mobileMenu = document.getElementById('mobileMenu');

    menuBtn.addEventListener('click', () => {
      mobileMenu.classList.toggle('active');
    });

    // DARK/LIGHT MODE
    const themeBtns = [
      document.getElementById('themeToggle'),
      document.getElementById('themeToggleMobile')
    ];

    themeBtns.forEach(btn => {
      btn.addEventListener('click', () => {
        document.body.classList.toggle('light');

        const isLight = document.body.classList.contains('light');

        themeBtns.forEach(b => {
          b.innerHTML = isLight
            ? '<i class="fa-solid fa-sun"></i>'
            : '<i class="fa-solid fa-moon"></i>';
        });
      });
    });

    // SCROLL ANIMATION
    const observer = new IntersectionObserver((entries)=>{
      entries.forEach(entry=>{
        if(entry.isIntersecting){
          entry.target.classList.add('show');
        }
      });
    }, {threshold:0.15});

    document.querySelectorAll('.fade-up').forEach(el=>{
      observer.observe(el);
    });

    // CONTACT FORM VALIDATION
    const form = document.getElementById('contactForm');
    const formMessage = document.getElementById('formMessage');

    form.addEventListener('submit', function(e){
      e.preventDefault();

      const name = document.getElementById('name').value.trim();
      const email = document.getElementById('email').value.trim();
      const phone = document.getElementById('phone').value.trim();
      const message = document.getElementById('message').value.trim();

      if(name.length < 3){
        formMessage.innerHTML = "Please enter a valid name.";
        formMessage.style.color = "#ef4444";
        return;
      }

      if(!email.includes('@')){
        formMessage.innerHTML = "Please enter a valid email.";
        formMessage.style.color = "#ef4444";
        return;
      }

      if(phone.length < 8){
        formMessage.innerHTML = "0745393259.";
        formMessage.style.color = "#ef4444";
        return;
      }

      if(message.length < 10){
        formMessage.innerHTML = "Message is too short.";
        formMessage.style.color = "#ef4444";
        return;
      }

      formMessage.innerHTML = "Inquiry submitted successfully!";
      formMessage.style.color = "#22c55e";

      form.reset();
    });

 </script>

<script type="module">
import { initializeApp } from "https://www.gstatic.com/firebasejs/10.12.2/firebase-app.js";
import { getAnalytics } from "https://www.gstatic.com/firebasejs/10.12.2/firebase-analytics.js";

const firebaseConfig = {
 apiKey: "AIzaSyAOo2cSdwAHeCxE5nyqmvUlSn-Fm92qmZI",
  authDomain: "smart-tots-school.firebaseapp.com",
  projectId: "smart-tots-school",
  storageBucket: "smart-tots-school.appspot.com",
  messagingSenderId: "823761166779",
  appId: "1:823761166779:web:fbebeab6a51e716e5f249e",
  measurementId: "G-NPFC39J976"
};

const app = initializeApp(firebaseConfig);
const analytics = getAnalytics(app);

console.log("Firebase connected");
</script>

</body>
</html>


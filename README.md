<!-- JAVASCRIPT -->
<script>

  // NAVBAR SCROLL
  const navbar = document.getElementById('navbar');

  window.addEventListener('scroll', () => {
    if(window.scrollY > 50){
      navbar.classList.add('nav-scrolled');
    } else {
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
  }, { threshold: 0.15 });

  document.querySelectorAll('.fade-up').forEach(el=>{
    observer.observe(el);
  });

</script>

<script type="module">

import { initializeApp } from "https://www.gstatic.com/firebasejs/10.12.2/firebase-app.js";

import {
  getFirestore,
  collection,
  addDoc
} from "https://www.gstatic.com/firebasejs/10.12.2/firebase-firestore.js";

const firebaseConfig = {
  apiKey: "AIzaSyAOo2cSdwAHeCxE5nyqmvUlSn-fM92qmZI",
  authDomain: "smart-tots-school.firebaseapp.com",
  projectId: "smart-tots-school",
  storageBucket: "smart-tots-school.appspot.com",
  messagingSenderId: "823761166779",
  appId: "1:823761166779:web:fbeab6a51e716e5f249e"
};

// FIREBASE
const app = initializeApp(firebaseConfig);
const db = getFirestore(app);

console.log("Firebase connected");

// FORM
const form = document.getElementById("contactForm");
const formMessage = document.getElementById("formMessage");

form.addEventListener("submit", async (e) => {

  e.preventDefault();

  const name = document.getElementById("name").value.trim();
  const email = document.getElementById("email").value.trim();
  const phone = document.getElementById("phone").value.trim();
  const message = document.getElementById("message").value.trim();

  // VALIDATION
  if(name.length < 2){
    formMessage.innerHTML = "Please enter a valid name.";
    formMessage.style.color = "#ef4444";
    return;
  }

  if(!email.includes("@")){
    formMessage.innerHTML = "Please enter a valid email.";
    formMessage.style.color = "#ef4444";
    return;
  }

  if(phone.length < 8){
    formMessage.innerHTML = "Please enter a valid phone number.";
    formMessage.style.color = "#ef4444";
    return;
  }

  if(message.length < 10){
    formMessage.innerHTML = "Message is too short.";
    formMessage.style.color = "#ef4444";
    return;
  }

  // SEND TO FIREBASE
  try {

    await addDoc(collection(db, "inquiries"), {
      name,
      email,
      phone,
      message,
      createdAt: new Date()
    });

    formMessage.innerHTML = "Inquiry submitted successfully!";
    formMessage.style.color = "#22c55e";

    form.reset();

  } catch(error){

    console.error(error);

    formMessage.innerHTML = "Error submitting inquiry.";
    formMessage.style.color = "#ef4444";
  }

});

</script>

</body>
</html>

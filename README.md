
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Portfolio - UPPARI VENKATESH</title>
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.1/css/all.min.css">
  <link rel="stylesheet" href="https://unpkg.com/aos@next/dist/aos.css" />
  <style>
  @import url('https://fonts.googleapis.com/css2?family=Poppins:wght@100;200;300;400;500;600&display=swap');
  
  *{
      padding: 0;
      margin: 0;
      font-family: 'Poppins', sans-serif;
      box-sizing: border-box;
  }

  body{
      width: 100%;
      min-height: 100vh;
      background-color: black;
      overflow-x: hidden;
  }

  html {
      scroll-behavior: smooth;
  }

  /* ---------- NAVBAR ---------- */

  nav {
    width: 100%;
    height: 10vh;
    position: sticky;
    top: 0;
    background-color: rgba(0, 0, 0, 0.8);
    backdrop-filter: blur(5px);
    z-index: 999;
  }

  .nav-container{
      width: 100%;
      height: 100%;
      display: flex;
      justify-content: space-around;
      align-items: center;
  }
  
  .logo{
      color: white;
      font-size: 1.5rem;
      font-weight: bold;
  }
  
  .logo span{
      color: rgb(211,3,3);
      text-shadow: 0 0 10px rgb(211,3,3);
  }
  
  .hamburg,
  .cancel{
      cursor: pointer;
      position: absolute;
      right: 15px;
      top: 10px;
      color: white;
      display: none;
      font-size: clamp(2.5rem, 0.5rem + 5vw, 3rem);
  }
  
  .nav-container .links {
      display: flex;
  }
  
  .nav-container .links a{
      font-size: 1.2rem;
      color: white;
      margin: 0 20px;
      text-decoration: none;
      font-weight: 550;
      transition: 0.3s linear;
  }
  
  .nav-container .links a:hover{
      color: rgb(211,3,3);
      border-bottom: 2px solid rgb(211,3,3);
  }
  
  .dropdown{
      z-index: 100;
      position: absolute;
      top: 0;
      transform: translateY(-500px);
      width: 100%;
      height: auto;
      backdrop-filter: blur(4px) brightness(40%);
      box-shadow: 0 0 20px black;
      transition: 0.2s linear;
  }
  
  .dropdown .links a{
      display: flex;
      color: white;
      text-decoration: none;
      padding: 15px 0;
      justify-content: center;
      align-items: center;
      transition: 0.2s linear;
  }
  
  .dropdown .links a:hover{
      background-color: rgb(211,3,3);
  }

  /* ---------- GENERIC SECTION ---------- */

  section{
      width: 100%;
      /* IMPORTANT: no fixed height here */
      padding-top: 40px;
      padding-bottom: 40px;
  }

  /* ---------- HOME SECTION ---------- */

  .main-container{
      width: 100%;
      min-height: 90vh;
      display: flex;
      justify-content: space-evenly;
      align-items: center;
  }
  
  .main-container .content{
      color: white;
      width: 40%;
      min-height: 100px;
  }
  
  .content h1 {
      font-size: clamp(0.8rem, 1rem + 2vw, 1.2rem);
  }
  
  .content h1 span{
      font-weight: 700;
      text-shadow: 0 0 10px rgb(211,3,3);
      color: rgb(211,3,3);
  }
  
  .content .typewriter{
      font-size: clamp(2rem, 2rem + 4vw, 2rem);
      font-weight: 700;
  }
  
  .typewriter span{
      color: rgb(211,3,3);
      text-shadow: 0 0 10px rgb(211,3,3);
  }
  
  .content p{
      font-size: clamp(0.4rem, 0.2rem + 9vw, 1rem);
      margin: 10px 0;
  }
  
  .social-links i{
    display: inline-flex;
    justify-content: center;
    align-items: center;
    width: 3rem;
    height: 3rem;
    background-color: transparent;
    border: 0.2rem solid rgb(211,3,3);
    border-radius: 50%;
    color: rgb(211,3,3);
    margin: 0 15px;
    font-size: 1.5rem;
    transition: transform 0.2s, box-shadow 0.2s, background-color 0.2s, color 0.2s;
  }

  .social-links i:hover{
    transform: scale(1.3);
    box-shadow: 0 0 15px rgb(211,3,3);
    background-color: rgb(211,3,3);
    color: black;
  }

  .content button{
    width: 50%;
    height: 6vh;
    margin: 30px;
    background-color: rgb(211,3,3);
    color: white;
    border: none;
    outline: none;
    font-size: 120%;
    font-weight: 700;
    border-radius: 5px;
    transition: transform 0.2s, box-shadow 0.2s, color 0.2s, border 0.2s, background-color 0.2s;
  }

  .content button:hover{
    transform: scale(1.1);
    color: rgb(211,3,3);
    border: 2px solid rgb(211,3,3);
    background-color: transparent;
    box-shadow: 0 0 40px 5px rgb(211,3,3);
  }

  .main-container .image{
      width: 300px;
      height: 300px;
      border-radius: 100%;
      overflow: hidden;
      box-shadow: 0 0 50px rgb(211,3,3);
  }
  
  .main-container .image img{
      width: 100%;
  }
  
  .main-container .image:hover{
      animation: animate 1.5s ease-in-out infinite;
  }
  
  @keyframes animate {
      0%{ scale: 1; }
      50%{ scale: 1.05; }
      100%{ scale: 1; }
  }

  .scroll-down-button {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    position: absolute;
    right: 50%;
    bottom: 30px;
    transform: translateX(50%);
    color: rgb(211,3,3);
    text-decoration: none;
    font-size: 1.5rem;
    animation: bounce 2s infinite;
    z-index: 2;
  }

  .scroll-down-button i {
    font-size: 1.8rem;
  }

  .scroll-down-button .scroll-text {
    color: rgb(211,3,3);
    font-size: 0.7rem;
    text-align: center;
    text-shadow: 0 0 5px rgb(211,3,3);
  }

  @keyframes bounce {
    0%, 100% { transform: translateX(50%) translateY(0); }
    50% { transform: translateX(50%) translateY(8px); }
  }

  /* ---------- RESUME SECTION ---------- */

  #resume-section {
    background: linear-gradient(135deg, #000000, #1a1a1a, #000000);
    color: white;
    padding: 50px 20px;
    text-align: center;
    position: relative;
    overflow: hidden;
  }

  #resume-section h2 {
    font-size: 2rem;
    margin-bottom: 20px;
    color: rgb(211,3,3);
    text-shadow: 0 0 10px rgb(211,3,3);
  }

  .resume-card {
    display: inline-block;
    background: #111;
    border: 2px solid rgb(211,3,3);
    border-radius: 12px;
    padding: 20px;
    box-shadow: 0 0 20px rgb(211,3,3);
    transition: transform 0.3s;
  }
  
  .resume-card:hover {
    transform: scale(1.05);
  }
  
  .resume-card img {
    width: 280px;
    max-width: 90%;
    border-radius: 6px;
    margin-bottom: 10px;
  }

  .abstract-background {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    z-index: 0;
  }

  .abstract-background svg {
    width: 100%;
    height: 100%;
  }

  .resume-container {
    position: relative;
    z-index: 1;
  }

  .resume-flex {
    display: flex;
    justify-content: center;
    align-items: center;
    gap: 30px;
    flex-wrap: wrap;
  }

  .robot-container {
    margin-top: 50px;
  }

  .robot-container img {
    height: 400px;
    width: auto;
    border-radius: 12px;
  }

  /* ---------- ABOUT & SKILLS ---------- */

  #about, #skills, #projects, #certificates {
    scroll-margin-top: 10vh;
  }

  .skills-section {
    padding: 50px;
    background: #000;
    color: #fff;
  }

  .section-title {
    text-align: center;
    font-size: 2rem;
    color: #ff0057;
    margin-bottom: 30px;
  }

  .skills-container {
    display: flex;
    justify-content: space-between;
    flex-wrap: wrap;
  }

  .technical-skills, .professional-skills {
    flex: 1;
    min-width: 300px;
    margin: 20px;
  }

  h3 {
    text-align: center;
    color: #ff0057;
    margin-bottom: 20px;
  }

  .skill {
    margin-bottom: 15px;
    text-align: center;
  }

  .skill-name {
    display: block;
    margin-bottom: 5px;
    color: #fff;
  }

  .skill-bar {
    background: #333;
    border-radius: 20px;
    overflow: hidden;
    height: 14px;
    width: 50%; 
    margin: auto;
  }

  .skill-bar-fill {
    background: linear-gradient(90deg, #ff0057, orange);
    height: 100%;
    width: 0;
    color: black;
    font-size: 12px;
    text-align: right;
    padding-right: 5px;
    border-radius: 20px;
    transition: width 2s;
  }

  .professional-skills {
    padding: 30px 0;
    text-align: center;
  }

  .professional-skills h3 {
    color: rgb(211,3,3);
    font-size: 1.8rem;
    margin-bottom: 40px;
    text-shadow: 0 0 8px rgb(211,3,3);
  }

  .technical-skills {
    padding: 30px 0;
    text-align: center;
  }

  .technical-skills h3 {
    color: rgb(211,3,3);
    font-size: 1.8rem;
    margin-bottom: 40px;
    text-shadow: 0 0 8px rgb(211,3,3);
  }

  .skills-gif {
    display: flex;
    justify-content: center;
    align-items: center;
    margin: 20px auto;
  }

  /* ---------- PROJECTS SECTION ---------- */
/* ---------- PROJECTS SECTION ---------- */

#projects {
  background-color: #111;
  color: white;
  padding: 60px 20px;
}

.projects-container h2 {
  font-size: 2rem;
  margin-bottom: 30px;
  color: rgb(211,3,3);
  text-shadow: 0 0 10px rgb(211,3,3);
  text-align: center;
}

/* GRID (3 cards desktop, 2 tab, 1 mobile) */
.projects-list {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 26px;
  max-width: 1150px;
  margin: 0 auto;
}

/* CARD STYLE (same theme as your website) */
.project-card {
  background: linear-gradient(180deg, rgba(25,25,25,0.98), #0e0e0e);
  border-radius: 14px;
  padding: 25px;
  border: 1px solid rgba(211,3,3,0.07);
  box-shadow: 0 8px 25px rgba(0,0,0,0.7);
  transition: 0.3s ease-in-out;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  height: 100%;
}

.project-card:hover {
  transform: translateY(-7px);
  border-color: rgba(211,3,3,0.2);
  box-shadow: 0 12px 40px rgba(211,3,3,0.08);
}

/* TOP ICON */

.icon-wrap {
  width: 100%;
  height: 170px;
  border-radius: 12px;
  background: rgba(255,255,255,0.04);
  border: 1px solid rgba(255,255,255,0.08);
  display: flex;
  align-items: center;
  justify-content: center;
  margin-bottom: 18px;
  overflow: hidden; 
}
.icon-wrap img {
  width: 100%;
  height: 100%;
  object-fit: cover; 
  display: block;
}


/* PROJECT TITLE */
.project-card h3 {
  font-size: 1.25rem;
  margin-bottom: 8px;
  color: rgb(211,3,3);
  font-weight: 700;
  text-shadow: 0 0 6px rgba(211,3,3,0.2);
}

/* DESCRIPTION */
.project-card p {
  font-size: 0.95rem;
  color: #d5d5d5;
  line-height: 1.5;
  margin-bottom: 14px;
}

/* TAGS */
.project-tags span {
  display: inline-block;
  padding: 6px 12px;
  font-size: 0.75rem;
  border-radius: 20px;
  margin-right: 6px;
  margin-bottom: 10px;
  color: rgb(211,3,3);
  border: 1px solid rgba(211,3,3,0.3);
  background: rgba(211,3,3,0.08);
}

/* BUTTON ROW */
.actions {
  margin-top: auto;
  display: flex;
  gap: 12px;
}

/* BUTTONS */
.btn-pill {
  padding: 10px 16px;
  border-radius: 12px;
  text-decoration: none;
  font-weight: 700;
  font-size: 0.9rem;
  display: inline-flex;
  align-items: center;
  gap: 6px;
  transition: 0.2s;
}



/* Dark = Code */
.btn-code {
  background: rgba(255,255,255,0.08);
  color: white;
  border: 1px solid rgba(255,255,255,0.15);
}

.btn-pill:hover {
  transform: translateY(-3px);
}

/* RESPONSIVE */
@media (max-width:1000px) {
  .projects-list {
    grid-template-columns: repeat(2, 1fr);
  }
}
@media (max-width:680px) {
  .projects-list {
    grid-template-columns: 1fr;
  }
}



  /* ---------- CERTIFICATES SECTION ---------- */

  #certificates {
    background-color: #111;
    color: white;
    padding: 60px 20px;
  }

  .certificates-container {
    max-width: 1200px;
    margin: auto;
    text-align: center;
  }

  .certificates-container h2 {
    font-size: 2rem;
    margin-bottom: 30px;
    color: rgb(211,3,3);
  }

  .certificates-list {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    gap: 20px;
  }

  .certificate {
    background: #222;
    border: 1px solid rgb(211,3,3);
    border-radius: 10px;
    padding: 15px;
    width: 250px;
    transition: transform 0.3s;
  }

  .certificate img {
    width: 100%;
    border-radius: 5px;
  }

  .certificate h3 {
    margin-top: 10px;
    font-size: 1.1rem;
    color: rgb(211,3,3);
  }

  .certificate p {
    font-size: 0.9rem;
  }

  .certificate:hover {
    transform: scale(1.05);
    box-shadow: 0 0 10px rgb(211,3,3);
  }

  /* ---------- FOOTER ---------- */

  footer {
    background-color: #000;
    color: white;
    padding: 30px 15px;
    text-align: center;
    border-top: 1px solid rgb(211,3,3);
    position: relative;
    overflow: hidden;
  }

  .footer-name {
    font-size: 1.8rem;
    font-weight: bold;
    margin-bottom: 10px;
    color: white;
    text-shadow: 0 0 8px rgb(211,3,3);
    transition: text-shadow 0.3s;
  }

  .footer-name span {
    color: rgb(211,3,3);
    text-shadow: 0 0 10px rgb(211,3,3);
  }

  .footer-name:hover {
    text-shadow: 0 0 15px rgb(211,3,3), 0 0 25px rgb(211,3,3);
  }

  .footer-quote {
    font-style: italic;
    font-size: 1rem;
    color: #aaa;
    margin-bottom: 10px;
    transition: color 0.3s;
  }

  .footer-quote:hover {
    color: rgb(211,3,3);
  }

  .back-to-top {
    display: inline-block;
    margin-bottom: 15px;
    color: rgb(211,3,3);
    text-decoration: none;
    font-weight: 500;
    transition: color 0.3s, text-shadow 0.3s;
  }

  .back-to-top i {
    margin-right: 5px;
  }

  .back-to-top:hover {
    color: white;
    text-shadow: 0 0 10px rgb(211,3,3);
  }

  .footer-copy {
    font-size: 0.9rem;
    color: #888;
  }
  /* Footer social icons - red style */
.footer-social-links {
  display: flex;
  justify-content: center;
  gap: 12px;
  margin: 12px 0 18px;
  z-index: 2;
}

.footer-social-links a {
  text-decoration: none;
  display: inline-flex;
  align-items: center;
  justify-content: center;
  width: 46px;
  height: 46px;
  border-radius: 10px;           /* change to 50% for circular icons */
  background: transparent;
  border: 1px solid rgba(211,3,3,0.15);
  transition: transform 0.18s, box-shadow 0.18s, background-color 0.18s, color 0.18s;
}

/* icon color + sizing */
.footer-social-links a i {
  color: rgb(211,3,3);
  font-size: 1.1rem;
  width: 100%;
  height: 100%;
  display: inline-flex;
  align-items: center;
  justify-content: center;
}

/* hover: filled red with dark icon */
.footer-social-links a:hover {
  transform: translateY(-4px) scale(1.04);
  background: rgb(211,3,3);
  border-color: rgb(211,3,3);
  box-shadow: 0 6px 18px rgba(211,3,3,0.12);
}
.footer-social-links a:hover i {
  color: #000;
}

/* Ensure footer icon color wins over other icon rules */
.footer-social-links a i { color: rgb(211,3,3) !important; }

/* Optional: make icons circular (uncomment if you want) */
/*
.footer-social-links a {
  border-radius: 50%;
}
*/


  /* ---------- ROBOT ---------- */

  #robo-container {
      transform: scale(0.6);
  }

  .robot {
      display: flex;
      flex-direction: column;
      align-items: center;
  }

  .head {
      width: 120px;
      height: 100px;
      background: #111;
      border: 5px solid #ccc;
      border-radius: 30px;
      position: relative;
      display: flex;
      justify-content: center;
      align-items: center;
      transform-style: preserve-3d;
      transition: transform 0.1s ease-out;
      box-shadow: 0 6px 15px rgba(0,0,0,0.4);
  }

  .eye {
      width: 20px;
      height: 20px;
      background: radial-gradient(circle, #4fc3f7, #0288d1);
      border-radius: 50%;
      position: absolute;
      top: 30px;
      transition: transform 0.1s ease-out;
      box-shadow: 0 0 10px #03a9f4;
  }
  .eye.left { left: 30px; }
  .eye.right { right: 30px; }

  .mouth {
      position: absolute;
      bottom: 20px;
      width: 35px;
      height: 15px;
      border-bottom: 2px solid #4fc3f7;
      border-radius: 50%;
  }

  .body {
      margin-top: 10px;
      width: 120px;
      height: 120px;
      background: linear-gradient(180deg, #f9fafb, #d1d5db);
      border-radius: 15px;
      position: relative;
      box-shadow: 0 5px 15px rgba(0,0,0,0.3);
      display: flex;
      justify-content: center;
      align-items: center;
      text-align: center;
      padding: 10px;
  }

  .body-text {
      font-size: 14px;
      font-weight: bold;
      color: #111;
      font-family: Arial, sans-serif;
  }

  .arm {
      width: 20px;
      height: 80px;
      background: #ccc;
      border-radius: 20px;
      position: absolute;
      top: 20px;
      transform-origin: top center;
      transition: transform 0.2s ease-out;
  }
  .arm.left { left: -25px; }
  .arm.right { right: -25px; }

  .leg {
      width: 30px;
      height: 60px;
      background: #bbb;
      border-radius: 15px;
      position: absolute;
      bottom: -60px;
  }
  .leg.left { left: 15px; }
  .leg.right { right: 15px; }

  /* ---------- RESPONSIVE ---------- */

  @media (max-width:884px) {
      nav .logo{
          position: absolute;
          top: 16px;
          left: 15px;
          font-size: 1.5rem;
      }
      .main-container{
          flex-direction: column-reverse;
      }
      .nav-container .links{
          display: none;
      }
      .hamburg, .cancel{
          display: block;
      }
      .main-container .content{
          width: 80%;
      }
      .social-links i{
          width: 2.5rem;
          height: 2.5rem;
          font-size: 1.5rem;
      }
      .main-container .image{
          z-index: -1;
          width: 50%;
          height: 60%;
      }
  }

  @media (max-width:440px) {
      .main-container .image{
          width: 70%;
          height: 60%;
      }
      .main-container .content{
          width: 80%;
      }
      .main-container button{
          margin-top: 15px;
      }
  }

  /* Mobile: 1 project per row */
  @media (max-width: 768px) {
    .project-card {
      flex: 1 1 100%;
      max-width: 500px;
    }
    
@keyframes bounce {
  0%, 100% { transform: translateX(50%) translateY(0); }
  50% { transform: translateX(50%) translateY(8px); }
}

    </style>
    
</head>
<body>

<nav>
  <div class="nav-container">
    <div class="logo" data-aos="zoom-in" data-aos-duration="1500">UPPARI VENKATESH <span></span></div>
    <div class="links">
      <a href="#home">Home</a>
      <a href="#about">About</a>
      <a href="#skills">Skills</a>
      <a href="#projects">Projects</a>
      <a href="#certificates">Certificates</a>
    </div>
    <div class="hamburg" onclick="hamburg()"><i class="fa-solid fa-bars"></i></div>
    <div class="cancel" onclick="cancel()"><i class="fa-solid fa-xmark"></i></div>
  </div>
  <div class="dropdown">
    <div class="links">
      <a href="#home">Home</a>
      <a href="#about">About</a>
      <a href="#skills">Skills</a>
      <a href="#certificates">Certificates</a>
    </div>
  </div>
</nav>

<section id="home">
  <div class="main-container">
    <div class="content" data-aos="fade-right" data-aos-duration="1500" data-aos-delay="300">
      
      
    
      <div data-aos="fade-right" data-aos-duration="1500" data-aos-delay="900" class="typewriter">
        Hey I'm <span class="typewriter-text"></span><label>|</label>
      </div>
      <h1 data-aos="fade-left" data-aos-duration="1500" data-aos-delay="700">I am a <span>STUDENT</span></h1>
      
      <p data-aos="flip-down" data-aos-duration="1500" data-aos-delay="1100">
        Passionate B.Tech student specializing in Computer Science and Engineering with a focus on Cloud computing & DEVOPS and Machine Learning.
      </p>
      <div class="social-links" data-aos="fade-right" data-aos-duration="1500" data-aos-delay="300">
        
        <a href="mailto:upparivenkatesh987@gmail.com" target="_blank"><i class="fa-solid fa-envelope"></i></a>
        <a href="https://www.linkedin.com/in/upparivenkatesh/" target="_blank"><i class="fa-brands fa-linkedin"></i></a>
        <a href="https://github.com/venkateshuppari" target="_blank"><i class="fa-brands fa-github"></i></a>
        <a href="https://x.com/home" target="_blank"><i class="fa-brands fa-twitter"></i></a>
      </div>
      
      
      <div class="btn" data-aos="fade-right" data-aos-duration="1500" data-aos-delay="300">
        <a href="#resume-section"><button>View My Resume</button></a>
      </div>
    </div>
    
    
    <div id="robo-container">
      <div class="robot">
        <div class="head" id="head">
          <div class="eye left" id="eyeLeft"></div>
          <div class="eye right" id="eyeRight"></div>
          <div class="mouth"></div>
        </div>
        <div class="body">
          <div class="arm left" id="armLeft"></div>
          <div class="arm right" id="armRight"></div>
          <div class="leg left"></div>
          <div class="leg right"></div>
          <div class="body-text">I’m Watching You 👀<br>Be Careful 😉</div>
        </div>
      </div>
    </div>
    
    <a href="#" class="scroll-down-button">
      <i class="fa-solid fa-angles-down"></i>
      <div class="scroll-text">Scroll Down</div>
    </a>
    <div class="image" data-aos="zoom-in" data-aos-duration="3000">
      <img src="https://i.postimg.cc/j5Wr9Z6D/Chat-GPT-Image-Feb-9-2026-10-15-47-AM.png" alt="uppari venkatesh">
    </div>
  </div>
  
</section>

<section id="resume-section">
  <div class="abstract-background">
    <svg viewBox="0 0 1440 320" preserveAspectRatio="none">
      <path fill="rgb(211,3,3)" fill-opacity="0.2"
        d="M0,128L48,128C96,128,192,128,288,144C384,160,480,192,576,197.3C672,203,768,181,864,170.7C960,160,1056,160,1152,165.3C1248,171,1344,181,1392,186.7L1440,192L1440,0L1392,0C1344,0,1248,0,1152,0C1056,0,960,0,864,0C768,0,672,0,576,0C480,0,384,0,288,0C192,0,96,0,48,0L0,0Z">
      </path>
    </svg>
  </div>
  <div class="resume-container" data-aos="fade-up" data-aos-duration="1500">
    <h2>My Resume</h2>
    <div class="resume-flex">
      <div class="robot-container">
        <img src="https://i.postimg.cc/gjtx6hwd/output-onlinegiftools.gif" alt="Robot">
      </div>
      <div class="resume-card">
  <a href="https://docs.google.com/document/d/1IyCpX-AP4LCxLWA6n19-vYT4SdA8N2QECfWBYOskH_s/edit?usp=drivesdk" target="_blank">
    <img 
      src="https://i.postimg.cc/Xvb8tJw3/cv-screen-shot.png" 
      alt="My Resume"
      style="cursor: pointer;"
    >
  </a>

  <a href="https://docs.google.com/document/d/1IyCpX-AP4LCxLWA6n19-vYT4SdA8N2QECfWBYOskH_s/edit?usp=drivesdk" target="_blank"></a>
    <p>Click for clear view</p>
  
</div>
    </div>
  </div>
</section>

  <section id="about" style="background: linear-gradient(135deg, #000000, #1a1a1a, #000000); color: white; padding: 50px 20px; text-align: center;">
  <div class="about-container" data-aos="fade-up" data-aos-duration="1500">
    <h2 style="font-size: 2rem; margin-bottom: 20px; color: rgb(211,3,3); text-shadow: 0 0 10px rgb(211,3,3);">
      About Me
    </h2>
    <p style="max-width: 800px; margin: auto; font-size: 1rem; line-height: 1.8;">
      Hi! I’m <span style="color: rgb(211,3,3); font-weight: 600;">Uppari venkatesh</span>, currently pursuing my B.Tech in Computer Science and Engineering with a specialization in Cloud & DEVOPs Engineer and Machine Learning.
    </p>
    <p style="max-width: 800px; margin: auto; font-size: 1rem; line-height: 1.8; margin-top: 10px;">
      I’m passionate about exploring how technology can solve real‑world problems, especially through Cloud and DEVOPS solutions. I enjoy designing Cloud applications, building clean web services, and constantly learning new skills to grow as a developer.
    </p>
    <p style="max-width: 800px; margin: auto; font-size: 1rem; line-height: 1.8; margin-top: 10px;">
      Apart from coding, I love playing cricket, following the latest tech trends, and experimenting with creative design projects.
    </p>
    <p style="max-width: 800px; margin: auto; font-size: 1rem; line-height: 1.8; margin-top: 10px;">
      My goal is to keep learning, collaborate with like‑minded people, and contribute to innovative projects that can make a difference.
    </p>
  </div>
</section>


<section id="skills" class="skills-section">
  <h3 class="section-title">Skills</h3>
  <div class="skills-container">
    <!-- Technical Skills -->
    <div class="technical-skills">
      <h3>Technical Skills</h3>
      <div class="skill">
        <span class="skill-name">C, C++</span>
        <div class="skill-bar">
          <div class="skill-bar-fill" data-percent="85">0%</div>
        </div>
      </div>
      <div class="skill">
        <span class="skill-name">HTML, CSS, JavaScript</span>
        <div class="skill-bar">
          <div class="skill-bar-fill" data-percent="80">0%</div>
        </div>
      </div>
      <div class="skill">
        <span class="skill-name">Python</span>
        <div class="skill-bar">
          <div class="skill-bar-fill" data-percent="90">0%</div>
        </div>
      </div>
      <div class="skill">
        <span class="skill-name">Java</span>
        <div class="skill-bar">
          <div class="skill-bar-fill" data-percent="85">0%</div>
        </div>
      </div>
      <div class="skill">
        <span class="skill-name">DSA</span>
        <div class="skill-bar">
          <div class="skill-bar-fill" data-percent="70">0%</div>
        </div>
      </div>
    </div>
    
    
    <div class="skills-gif">
      <img src="https://res.cloudinary.com/do3wub817/image/upload/v1756131927/video_20250825_193848_edit-ezgif.com-video-to-gif-converter_syhcvw.gif" alt="Skills Animation" width="350">

    </div>

    <!-- Professional Skills -->
    <div class="professional-skills">
      <h3>Professional Skills</h3>
      <div class="skill">
        <span class="skill-name">Communication</span>
        <div class="skill-bar">
          <div class="skill-bar-fill" data-percent="80">0%</div>
        </div>
      </div>
      <div class="skill">
        <span class="skill-name">Teamwork</span>
        <div class="skill-bar">
          <div class="skill-bar-fill" data-percent="85">0%</div>
        </div>
      </div>
      <div class="skill">
        <span class="skill-name">Creativity</span>
        <div class="skill-bar">
          <div class="skill-bar-fill" data-percent="75">0%</div>
        </div>
      </div>
      <div class="skill">
        <span class="skill-name">Leadership</span>
        <div class="skill-bar">
          <div class="skill-bar-fill" data-percent="90">0%</div>
        </div>
        </div>
        <div class="skill">
        <span class="skill-name">Problem-Solving</span>
        <div class="skill-bar">
          <div class="skill-bar-fill" data-percent="85">0%</div>
        </div>
      </div>
  </div>
</section>


<section id="projects">
  <div class="projects-container" data-aos="fade-up" data-aos-duration="1500">

    <h2>My Projects</h2>

    <div class="projects-list">

      <!-- PROJECT 1 -->
      <div class="project-card" data-aos="fade-up" data-aos-duration="1200">
        <div class="icon-wrap">
          <img src="https://i.postimg.cc/rs9Sx55K/image.png" alt="Fake Social-media Accounts Detection">
        </div>

        <h3>Fake Social-media Accounts Detection</h3>
        <p>
          A machine learning-based system that detects fake or bot social-media accounts using
          behavioral patterns and profile analysis. Built completely using Python.
        </p>

        <div class="project-tags">
          <span>Python</span>
          <span>ML</span>
          <span>Classification</span>
        </div>

        <div class="actions">
          <a href="https://github.com/venkateshuppari/Fake-Social-Media-Accounts-Detection"
             target="_blank" class="btn-pill btn-code">
            <i class="fa-brands fa-github"></i> Code
          </a>
        </div>
      </div> <!-- end project-card (Project 1) -->

      <!-- PROJECT 2 -->
      <div class="project-card" data-aos="fade-up" data-aos-duration="1200">
        <div class="icon-wrap">
          <img src="https://i.postimg.cc/J73GQ5xm/aaaaaa.png" alt="Aws-launcher-kit Project">
        </div>

        <h3>Aws-launcher-kit Project</h3>
        <p>
         A lightweight CLI-based toolkit to automate the deployment of EC2 instances using AWS CLI. This script simplifies instance instantiation, making cloud provisioning fast, repeatable, and hassle-free.  </p>

        <div class="project-tags">
          <span>Python</span>
          <span>Deep Learning</span>
          <span>CNN</span>
        </div>

        <div class="actions">
          <a href="https://github.com/venkateshuppari/AWS-Launcher-Kit"
             target="_blank" class="btn-pill btn-code">
            <i class="fa-brands fa-github"></i> Code
          </a>
        </div>
      </div> <!-- end project-card (Project 2) -->

      <!-- PROJECT 3 -->
      <div class="project-card" data-aos="fade-up" data-aos-duration="1200">
        <div class="icon-wrap">
          <img src="https://i.postimg.cc/XqtHq6PM/tttttt.png" alt="Deadlock-Prevention-and-Recovery-Toolkit-Project">
        </div>

        <h3>Deadlock-Prevention-and-Recovery-Toolkit Project</h3>
        <p>
          A security model that predicts Deadlock-Prevention-and-Recovery-Toolkit parameters, Security,
          Identity and  permission usage. Helps improve prevention Recovery-making.
        </p>

        <div class="project-tags">
          <span>Python</span>
          <span>ML</span>
          <span>Regression</span>
        </div>

        <div class="actions">
          <a href=" https://github.com/venkateshuppari/Deadlock-Prevention-and-Recovery-Toolkit"
             target="_blank" class="btn-pill btn-code">
            <i class="fa-brands fa-github"></i> Code
          </a>
        </div>
      </div> <!-- end project-card (Project 3) -->

    </div> <!-- end projects-list -->
  </div> <!-- end projects-container -->
</section>





    <section id="certificates">
      <div class="certificates-container" data-aos="fade-up" data-aos-duration="1500">
        <h2>My Certificates</h2>
        <div class="certificates-list">
          <div class="certificate">
            <img src="https://i.postimg.cc/W1wFb6FL/sssssssss.png" alt="Data Structure and Algorithms Certificate">
            <h3>Data Structure and Algorithms with Java</h3>
            <p>Issued by | CipherSchools |</p>
          </div>
          
          <div class="certificate">
            <img src="https://i.postimg.cc/4NGShsLp/gggggggggg.png" alt=" The Bits and Bytes of Computer Networking Certificate">
            <h3> The Bits and Bytes of Computer Networking</h3>
            <p> Authorized by | Google |</p>
          </div>
          
          <div class="certificate">
            <img src="https://i.postimg.cc/CKpBwrLd/nnnnnnn.png" alt="NPTEL Certificate">
            <h3>Generative Al Professional</h3>
            <p>Issued by | NPTEL  |</p>
          </div>
          
        <div class="certificate">
            <img src="https://i.postimg.cc/43PMXMb8/ccccccc.png" alt="Computer Communications Certificate">
            <h3>Computer Communications</h3>
            <p>Issued by | coursera  |</p>
      </div>
      
      
    </section>

<footer>
  <div class="footer-container">
    <h3 class="footer-name">UV<span>K😎</span></h3>
    <!-- Footer social icons -->
<div class="footer-social-links" aria-label="Footer social links">
  <a href="mailto:upparivenkatesh987@gmail.com" target="_blank" title="Email">
    <i class="fa-solid fa-envelope"></i>
  </a>
  <a href="www.linkedin.com/in/upparivenkatesh" target="_blank" title="LinkedIn">
    <i class="fa-brands fa-linkedin"></i>
  </a>
  <a href="https://github.com/venkateshuppari" target="_blank" title="GitHub">
    <i class="fa-brands fa-github"></i>
  </a>
  <a href="https://x.com/VenkateshU60866" target="_blank" title="X / Twitter">
    <i class="fa-brands fa-x-twitter"></i>
  </a>
</div>

    <p class="footer-quote">"💡 Small steps every day lead to big change."</p>
    <p class="footer-thankyou">Thank you for visiting my portfolio!</p>
    <a href="#home" class="back-to-top">
      <i class="fa-solid fa-arrow-up"></i> Back to Top
    </a>
    <p class="footer-copy">© 2025 uppari venkatesh. All rights reserved.</p>
  </div>
  
</footer>


<script src="https://unpkg.com/aos@next/dist/aos.js"></script>
<script>
  // Initialize AOS animation library
  AOS.init({ offset: 0 });
  
  // Mobile menu toggle functions
  function hamburg() {
    document.querySelector(".dropdown").style.display = "block";
    document.querySelector(".hamburg").style.display = "none";
    document.querySelector(".cancel").style.display = "block";
  }
  
  function cancel() {
    document.querySelector(".dropdown").style.display = "none";
    document.querySelector(".hamburg").style.display = "block";
    document.querySelector(".cancel").style.display = "none";
  }

  // Typewriter effect for hero section
  const textElement = document.querySelector(".typewriter-text");
  const texts = ["UPPARI VENKATESH"];
  let textIndex = 0;
  let charIndex = 0;
  let isDeleting = false;

  function type() {
    const currentText = texts[textIndex];
    if (isDeleting) {
      textElement.textContent = currentText.substring(0, charIndex - 1);
      charIndex--;
    } else {
      textElement.textContent = currentText.substring(0, charIndex + 1);
      charIndex++;
    }

    let typeSpeed = isDeleting ? 70 : 120;

    if (!isDeleting && charIndex === currentText.length) {
      typeSpeed = 1000;
      isDeleting = true;
    } else if (isDeleting && charIndex === 0) {
      isDeleting = false;
      textIndex = (textIndex + 1) % texts.length;
      typeSpeed = 500;
    }

    setTimeout(type, typeSpeed);
  }

  // Start typing animation after 1 second
  setTimeout(type, 1000);

  // Skills animation controller
  let skillsAnimated = false;
  const skillsSection = document.querySelector('.skills-section');
  
  function animateSkills() {
    // Animate technical skill bars
    const bars = document.querySelectorAll('.skill-bar-fill');
    bars.forEach(bar => {
      const percent = bar.getAttribute('data-percent');
      bar.style.width = '0%';
      let count = 0;
      const interval = setInterval(() => {
        if (count < percent) {
          count++;
          bar.style.width = count + '%';
          bar.textContent = count + '%';
        } else {
          clearInterval(interval);
        }
      }, 20);
    });

    
    
    skillsAnimated = true;
  }

  // Check if skills section is in view
  function checkSkillsVisibility() {
    if (skillsAnimated) return;
    
    const sectionTop = skillsSection.getBoundingClientRect().top;
    const sectionBottom = skillsSection.getBoundingClientRect().bottom;
    
    if (sectionTop < window.innerHeight && sectionBottom > 0) {
      animateSkills();
    }
  }

  // Set up scroll and load event listeners
  window.addEventListener('scroll', checkSkillsVisibility);
  window.addEventListener('load', checkSkillsVisibility);

  // Professional Skills Circle Animation with Intersection Observer
  document.addEventListener('DOMContentLoaded', function() {
    const circles = document.querySelectorAll('.circle-progress');
    
    const observer = new IntersectionObserver((entries) => {
      entries.forEach(entry => {
        if (entry.isIntersecting) {
          const circle = entry.target;
          const percent = parseInt(circle.parentElement.querySelector('.circle-text').textContent);
          let current = 0;
          
          const interval = setInterval(() => {
            if (current >= percent) {
              clearInterval(interval);
            } else {
              current++;
              circle.style.strokeDashoffset = `calc(283 - (283 * ${current}) / 100)`;
              circle.parentElement.querySelector('.circle-text').textContent = `${current}%`;
            }
          }, 20);
          
          observer.unobserve(entry.target);
        }
      });
    }, {threshold: 0.5});
    
    circles.forEach(circle => {
      observer.observe(circle);
    });
  });
  
  
  const head = document.getElementById("head");
    const eyeLeft = document.getElementById("eyeLeft");
    const eyeRight = document.getElementById("eyeRight");
    const armLeft = document.getElementById("armLeft");
    const armRight = document.getElementById("armRight");

    document.addEventListener("mousemove", (e) => {
      const { innerWidth, innerHeight } = window;
      const x = (e.clientX / innerWidth - 0.5) * 80;  
      const y = (e.clientY / innerHeight - 0.5) * 80;

      head.style.transform = `rotateY(${x}deg) rotateX(${-y}deg)`;

      const eyeX = (e.clientX / innerWidth - 0.5) * 35;
      const eyeY = (e.clientY / innerHeight - 0.5) * 35;
      eyeLeft.style.transform = `translate(${eyeX}px, ${eyeY}px)`;
      eyeRight.style.transform = `translate(${eyeX}px, ${eyeY}px)`;

      const robotCenterX = window.innerWidth / 2;
      if (e.clientX > robotCenterX) {
        armRight.style.transform = "rotate(-60deg)";
        armLeft.style.transform = "rotate(0deg)";
      } else {
        armLeft.style.transform = "rotate(60deg)";
        armRight.style.transform = "rotate(0deg)";
      }
    });
    
    
    
</script>

</body>
</html>











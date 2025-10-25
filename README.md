# Unaiza-Tanveer-portfolio
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="utf-8" />
<meta name="viewport" content="width=device-width,initial-scale=1" />
<title>Unaiza Tanveer | Portfolio</title>
<style>
*{box-sizing:border-box;margin:0;padding:0}
:root{
  --bg:#0a0a0a; --accent:#00bcd4; --muted:#cfcfcf;
  --card:rgba(255,255,255,0.05);
  --neon:#ffffff;
}
body{
  font-family:"Poppins",system-ui,Segoe UI,Roboto,Arial;
  background:var(--bg); color:#fff; overflow-x:hidden; cursor:none;
}
canvas{position:fixed;left:0;top:0;width:100%;height:100%;z-index:-1}
header{
  position:sticky;top:0;z-index:20; display:flex;align-items:center;justify-content:space-between;
  padding:14px 5%;backdrop-filter:blur(8px);
  background:linear-gradient(180deg, rgba(10,10,10,0.6), rgba(10,10,10,0.2));
  border-bottom:1px solid rgba(255,255,255,0.02);
}
.brand{display:flex;align-items:center;gap:12px}
.logo{
  width:44px;height:44px;border-radius:10px;
  background:linear-gradient(135deg,var(--accent),#7ce7f0);
  display:flex;align-items:center;justify-content:center;font-weight:700;color:#042;
  box-shadow:0 6px 18px rgba(0,188,212,0.08);
}
header h1{font-size:1.05rem;color:var(--accent);letter-spacing:0.4px}
nav{display:flex;gap:18px;align-items:center;flex-wrap:wrap}
nav a{color:#fff;text-decoration:none;font-size:0.95rem;opacity:0.95}
nav a:hover{color:var(--accent)}
.quick-contact{display:flex;gap:12px;align-items:center}
.quick-contact a{
  background:var(--card);padding:8px 12px;border-radius:999px;text-decoration:none;color:var(--muted);font-size:0.9rem;
}
.quick-contact a:hover{background:rgba(0,188,212,0.08);color:#fff;border:1px solid rgba(0,188,212,0.08);}
.hero{height:78vh;display:flex;align-items:center;justify-content:center;padding:3rem 5%;text-align:center}
.hero-inner{max-width:880px}
.hero h2{font-size:2.6rem;color:var(--accent);margin-bottom:8px}
.hero p{color:var(--muted);font-size:1.05rem;line-height:1.6}
.hero .cta{margin-top:20px;display:flex;gap:12px;justify-content:center;flex-wrap:wrap}
.btn {
  background: rgba(255,255,255,0.05); /* light transparent card style */
  color: var(--muted);
  padding: 12px 22px;
  border-radius: 12px; /* cuboid shape */
  text-decoration: none;
  font-weight: 600;
  box-shadow: 0 0 10px rgba(0,188,212,0.15); /* subtle neon glow */
  transition: all 0.3s ease;
}

.btn:hover {
  transform: translateY(-4px);
  box-shadow: 0 0 20px rgba(0,188,212,0.5), 0 0 40px rgba(0,188,212,0.2) inset; /* neon glowing hover */
  color: #fff;
  background: rgba(0,188,212,0.08); /* soft neon glow on hover */
}

/* Unified button / card style */
/* Unified button style */
.btn {
  background: rgba(255,255,255,0.05); /* subtle light shade */
  color: var(--muted);
  padding: 12px 22px;
  border-radius: 12px; /* cuboid shape */
  text-decoration: none;
  font-weight: 600;
  border: 1px solid rgba(255,255,255,0.2); /* thin white border */
  box-shadow: 0 0 10px rgba(0,188,212,0.15); /* subtle neon glow */
  transition: all 0.3s ease;
}

/* Hover effect - neon glow */
.btn:hover {
  transform: translateY(-4px);
  box-shadow: 0 0 20px rgba(0,188,212,0.5), 0 0 40px rgba(0,188,212,0.2) inset;
  background: rgba(0,188,212,0.08); /* soft neon glow */
  color: #fff;
}

section{padding:60px 5%}
h3{color:var(--accent);text-align:center;font-size:1.4rem;margin-bottom:14px}
.lead{color:var(--muted);max-width:900px;margin:8px auto 0;text-align:center}
.about-extra{margin-top:15px;color:var(--muted);font-size:1rem;line-height:1.6;}
.about-extra ul{list-style: inside disc;margin-top:10px;}
.about-extra li{margin-bottom:6px;}
.projects{display:grid;grid-template-columns:repeat(auto-fit,minmax(260px,1fr));gap:18px;margin-top:22px}
.project{background:var(--card);padding:18px;border-radius:14px;transition: transform 0.2s, box-shadow 0.3s;cursor:pointer;}
.project:hover{transform: translateY(-4px);box-shadow:0 12px 30px rgba(0,188,212,0.3);}
.project h4{color:var(--accent);margin-bottom:8px}
.project p{color:var(--muted);font-size:0.95rem;line-height:1.5}
.project .links{margin-top:12px;display:flex;gap:8px;flex-wrap:wrap}
.project .links a{padding:8px 12px;border-radius:999px;background:rgba(255,255,255,0.04);color:#fff;text-decoration:none;font-size:0.9rem}
.project .links a:hover{background:var(--accent);color:#001}
.cards{display:flex;gap:18px;flex-wrap:wrap;justify-content:center;margin-top:20px}
.card{background:var(--card);padding:18px;border-radius:12px;min-width:260px;max-width:480px}
.card strong{color:var(--accent)}
.resume a {
  display: inline-block;
  margin-top: 12px;
  padding: 12px 20px;       /* slightly bigger padding for balance */
  border-radius: 12px;      /* cuboid shape instead of oval */
  background: rgba(255,255,255,0.05);
  color: var(--muted);
  text-decoration: none;
  font-weight: 600;
  transition: all 0.3s ease;
  box-shadow: 0 0 10px rgba(0,188,212,0.15); /* subtle neon glow */
}

.resume a:hover {
  transform: translateY(-4px);
  box-shadow: 0 0 20px rgba(0,188,212,0.5), 0 0 40px rgba(0,188,212,0.2) inset; /* glowing hover */
  color: #fff;
  background: rgba(0,188,212,0.08);
}


.contact-card{
  max-width:760px;margin:30px auto;padding:25px;border-radius:12px;
  background:transparent;border:none;
  text-align:center; display:flex;flex-direction:column; gap:15px; align-items:center;
}
.contact-card p{color:var(--muted);line-height:1.8;text-align:center;font-size:1rem;}
.contact-card .links{display:flex;gap:15px;justify-content:center;flex-wrap:wrap;}
.contact-card a {
  padding:10px 18px;
  border-radius:12px;
  background:transparent; /* removes the white shade */
  text-decoration:none;
  color:var(--muted);
  transition: all 0.4s ease;
  box-shadow: 0 0 0 rgba(0,188,212,0); /* start with no glow */
}

.contact-card a:hover {
  transform: translateY(-5px);
  box-shadow: 0 0 20px rgba(0,188,212,0.5), 0 0 40px rgba(0,188,212,0.2) inset;
  color:#fff; /* brightens text */
}
.contact-card .links {
  display:flex;
  gap:15px;  /* This sets spacing between all links */
  justify-content:center;
  flex-wrap:wrap;
}

.skill-section{display:flex;flex-direction:column;align-items:center;gap:25px;margin-top:25px;}
.skill-container{display:flex;flex-wrap:wrap;justify-content:center;gap:15px;}
.skill-card{
  background:rgba(255,255,255,0.05);padding:16px 20px;border-radius:14px;
  min-width:160px;text-align:center;position:relative;
  transition: all 0.4s ease; cursor:pointer;
  box-shadow:0 0 10px rgba(0,188,212,0.15);
}
.skill-card:hover{
  transform: translateY(-5px);
  box-shadow:0 0 20px rgba(0,188,212,0.5),0 0 40px rgba(0,188,212,0.2) inset;
}
.skill-card h4{color:var(--accent);margin-bottom:6px;font-size:1rem;}
.skill-card p{font-size:0.85rem;color:var(--muted);line-height:1.2;}
footer{padding:28px 5%;text-align:center;color:#8f8f8f;font-size:0.9rem;margin-top:20px}
@media (max-width:720px){.hero{padding:2rem 4%}.hero h2{font-size:1.8rem}}
.cursor {width:18px;height:18px;border-radius:50%;border:2px solid var(--neon);position:fixed;top:0;left:0;pointer-events:none;box-shadow:0 0 8px var(--neon),0 0 16px var(--neon);transition: transform 0.1s ease-out;z-index:9999;}
.certificates{
  display:flex;
  flex-wrap:wrap;
  gap:16px;
  justify-content:center;
  margin-top:18px;
}

.cert-card{
  background:rgba(255,255,255,0.05);
  padding:14px 18px;
  border-radius:12px;
  transition:transform 0.2s, box-shadow 0.3s;
  text-align:center;
  min-width:180px;
  cursor:pointer;
}
.cert-card:hover{
  transform:translateY(-5px);
  box-shadow:0 0 20px rgba(0,188,212,0.5),0 0 40px rgba(0,188,212,0.2) inset;
}
.cert-card a{
  text-decoration:none;
  color:var(--muted);
  font-size:0.95rem;
}
.cert-card a:hover{
  color:#fff;
}
/* 🌟 CONTACT SECTION */
#contact {
  padding: 80px 0;
  text-align: center;
  color: #fff;
}

#contact h2 {
  font-size: 2rem;
  color: var(--accent);
  margin-bottom: 15px;
  letter-spacing: 0.5px;
}

#contact p {
  color: var(--muted);
  font-size: 1.05rem;
  max-width: 600px;
  margin: 0 auto 40px;
  line-height: 1.7;
}

/* Contact links container */
.contact-container {
  display: flex;
  justify-content: center;
  align-items: center;
  gap: 40px;
  flex-wrap: wrap;
  margin-bottom: 30px;
}

/* Individual contact links */
.contact-link {
  background: var(--card);
  padding: 14px 28px;
  border-radius: 999px;
  color: var(--muted);
  text-decoration: none;
  font-size: 1rem;
  transition: all 0.3s ease;
  display: flex;
  align-items: center;
  gap: 10px;
  box-shadow: none;
  border: 1px solid rgba(255, 255, 255, 0.05);
}

/* Hover effect — blue glowing animation like others */
.contact-link:hover {
  color: #fff;
  background: rgba(0, 188, 212, 0.1);
  box-shadow: 0 0 15px rgba(0, 188, 212, 0.4);
  transform: translateY(-3px);
  border-color: rgba(0, 188, 212, 0.2);
}

/* Icons inside contact links */
.contact-link i {
  font-size: 1.2rem;
  color: var(--accent);
}

/* Footer text under contact links */
.contact-footer {
  color: var(--muted);
  font-size: 1rem;
  margin-top: 20px;
  letter-spacing: 0.5px;
  opacity: 0.9;
}

/* 🧩 Responsive for small screens */
@media (max-width: 768px) {
  .contact-container {
    flex-direction: column;
    gap: 20px;
  }

  #contact h2 {
    font-size: 1.6rem;
  }

  .contact-link {
    padding: 12px 22px;
    font-size: 0.95rem;
  }
}


</style>
</head>
<body>

<canvas id="bg"></canvas>

<header>
  <div class="brand">
    <div class="logo">UT</div>
    <div>
      <h1>Unaiza Tanveer</h1>
      <div style="font-size:0.78rem;color:var(--muted)">Tech & AI Enthusiast — Web Developer</div>
    </div>
  </div>
  <nav>
    <a href="#about">About</a>
    <a href="#skills">Skills</a>
    <a href="#projects">Projects</a>
    <a href="#education">Education</a>
    <a href="#resume">Resume</a>
    <a href="#contact">Contact</a>
    <div class="quick-contact">
      <a href="https://mail.google.com/mail/?view=cm&fs=1&to=unaizatanveerr@gmail.com" target="_blank">✉️ Email</a>
      <a href="https://www.linkedin.com/in/unaizatanveer" target="_blank">in</a>
    </div>
  </nav>
</header>

<main>
<section class="hero">
  <div class="hero-inner">
    <h2>Hi, I'm Unaiza Tanveer</h2>
    <p class="lead">Tech & AI enthusiast with a passion for web development and creating meaningful, innovative solutions through technology. I focus on clean design, practical code, and AI-assisted projects.</p>
    <div class="cta">
      <a class="btn" href="#projects">See Projects</a>
      <a class="btn outline" href="#contact">Get in Touch</a>
    </div>
  </div>
</section>

<section id="about">
<h3>About Me</h3>
<p class="lead">I’m a Bachelor’s student in Computer Applications at Vaagdevi Degree and PG College (GPA: 8.9). I enjoy building web projects, learning AI/ML basics, and solving problems using programming and design.</p>
<div class="about-extra">
</div>
</section>

<section id="skills">
<h3>Skills</h3>
<div class="skill-section">
<h4 style="color:var(--accent);margin-bottom:10px;">Technical Skills</h4>
<div class="skill-container">
<div class="skill-card"><h4>HTML & CSS</h4><p>Web structure & styling</p></div>
<div class="skill-card"><h4>JavaScript</h4><p>Interactive web functionalities</p></div>
<div class="skill-card"><h4>C / C++ / Java</h4><p>Programming & problem solving</p></div>
<div class="skill-card"><h4>AI / ML Basics</h4><p>Machine Learning fundamentals</p></div>
<div class="skill-card"><h4>Data Structures</h4><p>Algorithmic thinking & efficiency</p></div>
<div class="skill-card"><h4>Git</h4><p>Version control & collaboration</p></div>
</div>

<h4 style="color:var(--accent);margin:20px 0 10px;">Soft Skills</h4>
<div class="skill-container">
<div class="skill-card"><h4>Leadership</h4><p>Guiding teams and projects</p></div>
<div class="skill-card"><h4>Communication</h4><p>Clear & effective communication</p></div>
<div class="skill-card"><h4>Teamwork</h4><p>Collaborative project work</p></div>
<div class="skill-card"><h4>Problem Solving</h4><p>Analyzing & solving challenges</p></div>
<div class="skill-card"><h4>Creativity</h4><p>Innovative & practical ideas</p></div>
</div>
</div>
</section>

<section id="projects">
<h3>Projects</h3>
<div class="projects">
<div class="project"><h4>Portfolio Website</h4><p>Developed this responsive portfolio using HTML, CSS, and JavaScript. Deployed on GitHub for recruiters and portfolio visitors.</p>
<div class="links">
  <a href="https://github.com/Unaiza-03/My-final-portfolio" target="_blank">🔗     View Repository</a>
</div>



<div class="links"></div></div>
<div class="project">
  <h4>AI-Powered Earbuds</h4>
  <p>Clay-based prototype integrating AI-powered features created during a design sprint at SR University. <strong>Led the team throughout the project.</strong></p>
  <div class="links">
    <a href="https://docs.google.com/presentation/d/1zu4GsdHq4Jtbb4y9N67LTo8S0dCEzYrk/view?usp=sharing" target="_blank">🎥 View Presentation</a>
  </div>
</div>

<div class="project"><h4>Cloud Computing Access Control</h4><p>Collaborated on encrypted cloud storage & access control — contributed to system analysis, documentation, and presentation.</p></div>

<div class="project"><h4>Gen AI Hackathon</h4><p>Built an AI-assisted web demo for “Demystifying Legal Documents” during a Gen AI hackathon using AI tools.</p>
<div class="links">
<a href="https://my-site-ho4vnx1n-fouziatarannum10.wix-vibe.com/" target="_blank">🌐 View Website</a>
<a href="https://docs.google.com/presentation/d/1vmdkNnh7tWuTczEPNQtoofXEskTnY9Td/view?usp=sharing" target="_blank">🎥 View Presentation</a>
</div></div>
</div>
</section>

<section id="education">
<h3>Education</h3>
<div class="cards">
<div class="card"><strong>Bachelor’s in Computer Applications</strong><div style="color:var(--muted)">Vaagdevi Degree and PG College, Hanamkonda — GPA: 8.9 (2023–2026)</div></div>
<div class="card"><strong>Diploma in Computer Science</strong><div style="color:var(--muted)">Bomma Institute of Technology and Science — CGPA: 9.75 (2020–2023)</div></div>
<div class="card"><strong>10th (SSC)</strong><div style="color:var(--muted)">Triveni Talent School — CGPA: 10 (2019–2020)</div></div>
</div>
</section>

<section id="certificates">
  <h3>Certificates</h3>
  <div class="certificates">
    <div class="cert-card">
      <a href="https://drive.google.com/file/d/1e58WIloKA7b3ouev7QSgtLeMcv-WgR2n/view?usp=sharing" target="_blank">
        12-week NPTEL C++ Course
      </a>
    </div>
    <div class="cert-card">
      <a href="https://drive.google.com/file/d/1JuamWrRgRHyKQddinipjavz3z9_uuLYk/view?usp=sharing" target="_blank">
        AI & ML Certification
      </a>
    </div>
    <div class="cert-card">
      <a href="https://drive.google.com/file/d/1DQVBffMoiRgGbHyX5TIqtVkZshjvVSED/view?usp=sharing" target="_blank">
        Young Turks 2025 by Naukri.com
      </a>
    </div>
  </div>
</section>


<section id="resume" class="resume">
  <h3>My Resume</h3>
  <p class="lead">Latest resume — click below to view or download.</p>
  <div style="text-align:center">
    <a href="https://docs.google.com/document/d/1mobvVMJIMNBh9jq-iloTogxkOj9b-w8s/edit?usp=sharing&ouid=109080723876500773613&rtpof=true&sd=true" 
       target="_blank" rel="noopener" aria-label="View resume">
       📄 View / Download Resume
    </a>
  </div>
</section>

<section id="contact" class="contact">
  <h2>📬 Let’s Connect</h2>
  <p>If you're looking for someone passionate, creative, and ready to bring ideas to life — I’d love to hear from you!</p>
  
 <div class="contact-container">
    <a href="https://mail.google.com/mail/?view=cm&fs=1&to=unaizatanveerr@gmail.com" target="_blank" class="contact-link">
      <i class="fa-solid fa-envelope"></i> Mail Me
    </a>

    <a href="https://linkedin.com/in/unaizatanveer" target="_blank" class="contact-link">
      <i class="fa-brands fa-linkedin"></i> LinkedIn
    </a>

    <a href="tel:+919398974719" class="contact-link">
      <i class="fa-solid fa-phone"></i> Contact    </a>
</div>

  <p class="contact-footer">Let’s build something amazing together 💻</p>
</section>


</main>

<footer>© 2025 Unaiza Tanveer — Built with code & passion.</footer>

<div class="cursor" id="cursor"></div>

<script>
// ---------------- Starry background ----------------
const canvas = document.getElementById('bg');
const ctx = canvas.getContext('2d');
let W = canvas.width = innerWidth;
let H = canvas.height = innerHeight;
window.addEventListener('resize',()=>{W=canvas.width=innerWidth;H=canvas.height=innerHeight;initStars();});

const starsArray=[];
function rand(min,max){return Math.random()*(max-min)+min}
function initStars(){
  starsArray.length=0;
  const count=Math.round((W*H)/7000);
  for(let i=0;i<count;i++){
    starsArray.push({x:rand(0,W),y:rand(0,H),r:rand(0.8,2.2),vx:rand(-0.2,0.2),vy:rand(-0.2,0.2)});
  }
}
function animateStars(){
  ctx.clearRect(0,0,W,H);
  for(const s of starsArray){
    s.x+=s.vx; s.y+=s.vy;
    if(s.x<0||s.x>W)s.vx*=-1;
    if(s.y<0||s.y>H)s.vy*=-1;
    ctx.beginPath();
    ctx.fillStyle='rgba(255,255,255,0.5)';
    ctx.arc(s.x,s.y,s.r,0,Math.PI*2);
    ctx.fill();
  }
  // Connecting stars
  for(let i=0;i<starsArray.length;i++){
    for(let j=i+1;j<starsArray.length;j++){
      let dx=starsArray[i].x-starsArray[j].x;
      let dy=starsArray[i].y-starsArray[j].y;
      let dist=Math.sqrt(dx*dx+dy*dy);
      if(dist<100){
        ctx.beginPath();
        ctx.moveTo(starsArray[i].x,starsArray[i].y);
        ctx.lineTo(starsArray[j].x,starsArray[j].y);
        ctx.strokeStyle='rgba(0,188,212,0.2)';
        ctx.stroke();
      }
    }
  }
  requestAnimationFrame(animateStars);
}
initStars();animateStars();

// ---------------- Cursor ----------------
const cursor=document.getElementById('cursor');
document.addEventListener('mousemove',e=>{
  cursor.style.transform=`translate(${e.clientX-9}px,${e.clientY-9}px)`;
});
</script>

</body>
</html>

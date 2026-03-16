<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Clarity Portfolio</title>
<link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;600;700&display=swap" rel="stylesheet">
<style>
html{scroll-behavior:smooth;}
*{box-sizing:border-box;margin:0;padding:0;font-family:'Inter',sans-serif;}

body{
background: radial-gradient(circle at 20% 30%, #6c63ff, transparent 50%),
            radial-gradient(circle at 80% 70%, #00cfff, transparent 50%),
            radial-gradient(circle at 50% 50%, #ff6ec4, transparent 50%),
            #0f0c29;
color:#fff;
min-height:100vh;
animation:moveBG 10s infinite alternate;
overflow-x:hidden;
}

@keyframes moveBG{
0%{background-position:20% 30%,80% 70%,50% 50%;}
100%{background-position:30% 40%,70% 60%,60% 40%;}
}

/* Header & Navbar */
header{
position:sticky;
top:0;
z-index:1000;
padding:15px 40px;
display:flex;
justify-content:space-between;
align-items:center;
background:rgba(255,255,255,0.05);
backdrop-filter:blur(10px);
border-radius:12px;
border:1px solid rgba(255,255,255,0.1);
}

.logo{font-size:24px;font-weight:700;}

nav{
display:flex;
gap:15px;
}

nav a{
text-decoration:none;
color:white;
margin-left:25px;
transition:0.3s;
}

nav a:hover{color:#6c63ff;}

.btn-hire{
padding:8px 20px;
border-radius:6px;
background:linear-gradient(90deg,#ff6ec4,#7873f5);
}

/* Hamburger Menu */
.hamburger{
display:none;
flex-direction:column;
cursor:pointer;
gap:5px;
}
.hamburger span{
display:block;
width:25px;
height:3px;
background:white;
border-radius:2px;
transition:0.3s;
}

/* Hero */
.hero{
display:flex;
align-items:center;
justify-content:space-between;
padding:80px 50px;
flex-wrap:wrap;
}

.hero-text{max-width:500px;}

.hero-text h1{
font-size:48px;
margin-bottom:20px;
}

.hero-text span{
background:linear-gradient(90deg,#6c63ff,#00cfff);
-webkit-background-clip:text;
-webkit-text-fill-color:transparent;
}

.hero-text p{color:#ccc;margin-bottom:30px;}

.btn-view{
padding:10px 25px;
border-radius:6px;
background:linear-gradient(90deg,#ff6ec4,#7873f5);
text-decoration:none;
color:white;
}

.hero-image img{
width:350px;
border-radius:10px;
box-shadow:0 0 80px #6c63ff;
}

/* Projects */
.projects{
display:flex;
justify-content:center;
gap:25px;
padding:50px;
flex-wrap:wrap;
}

.project-card{
background:rgba(255,255,255,0.05);
border:1px solid rgba(255,255,255,0.1);
border-radius:12px;
overflow:hidden;
width:300px;
transition:0.3s;
backdrop-filter:blur(10px);
}

.project-card img{
width:100%;
height:180px;
object-fit:cover;
}

.project-card .content{padding:20px;}

.project-card:hover{
transform:translateY(-10px);
box-shadow:0 0 25px #6c63ff;
}

/* Services */
.services{
padding:50px;
text-align:center;
}

.services-list{
display:flex;
justify-content:center;
gap:30px;
flex-wrap:wrap;
}

.service-item{
background:rgba(255,255,255,0.05);
padding:25px;
border-radius:12px;
width:220px;
transition:0.3s;
}

.service-item:hover{transform:translateY(-10px);}

/* Skills */
.skills{
padding:50px;
text-align:center;
}

.skill{
margin:20px auto;
width:300px;
text-align:left;
}

.bar{
background:#222;
border-radius:20px;
overflow:hidden;
}

.bar span{
display:block;
height:10px;
background:linear-gradient(90deg,#ff6ec4,#7873f5);
}

.html{width:90%;}
.css{width:80%;}
.js{width:60%;}

/* Contact */
.contact{
padding:60px 20px;
text-align:center;
}

.contact form{
max-width:500px;
margin:auto;
display:flex;
flex-direction:column;
gap:15px;
}

.contact input,
.contact textarea{
padding:12px;
border:none;
border-radius:8px;
background:rgba(255,255,255,0.05);
color:white;
}

.contact textarea{
height:120px;
resize:none;
}

.contact button{
padding:12px;
border:none;
border-radius:8px;
background:linear-gradient(90deg,#ff6ec4,#7873f5);
color:white;
font-weight:600;
cursor:pointer;
}

.contact button:hover{opacity:0.8;}

/* Reveal animation */
.reveal{
opacity:0;
transform:translateY(60px);
transition:0.8s;
}

.reveal.active{
opacity:1;
transform:translateY(0);
}

/* Mouse glow */
.cursor-glow{
position:fixed;
width:300px;
height:300px;
background:radial-gradient(circle,#6c63ff55,transparent 70%);
pointer-events:none;
border-radius:50%;
transform:translate(-50%,-50%);
z-index:0;
}

footer{
text-align:center;
padding:30px;
color:#aaa;
}

/* =================== MOBILE RESPONSIVENESS =================== */
@media (max-width: 1024px){
  header{padding:15px 20px;}
  nav{display:none; position:absolute; top:60px; right:20px; flex-direction:column; background:rgba(255,255,255,0.05); padding:15px; border-radius:12px; backdrop-filter:blur(10px);}
  nav.active{display:flex;}
  .hamburger{display:flex;}

  .hero{flex-direction:column; text-align:center; padding:60px 30px;}
  .hero-image img{width:80%; margin-top:30px;}

  .projects{flex-direction:column; align-items:center; padding:30px 20px;}
  .project-card{width:90%; max-width:350px; margin-bottom:20px;}

  .services-list{flex-direction:column; align-items:center;}
  .service-item{width:90%; max-width:300px; margin-bottom:20px;}

  .skills .skill{width:90%; max-width:350px;}
  .contact form{width:90%; max-width:400px;}
}

@media (max-width: 480px){
  .hero-text h1{font-size:32px;}
  .hero-text p{font-size:16px;}
  .btn-view, .btn-hire{padding:8px 16px; font-size:14px;}
  nav a{font-size:14px;}
}
</style>
</head>
<body>

<div class="cursor-glow"></div>

<header>
  <div class="logo">Clarity</div>
  <div class="hamburger" id="hamburger">
    <span></span>
    <span></span>
    <span></span>
  </div>
  <nav id="nav-links">
    <a href="#">Home</a>
    <a href="#projects">Projects</a>
    <a href="#services">Services</a>
    <a href="#contact">Contact</a>
    <a href="#" class="btn-hire">Hire Me</a>
  </nav>
</header>

<section class="hero reveal">
  <div class="hero-text">
    <h1>Hi, I'm <span id="typing"></span></h1>
    <p>I build modern websites and web apps.</p>
    <a href="#projects" class="btn-view">View My Work</a>
  </div>
  <div class="hero-image">
    <img src="https://i.ibb.co/JxqGfFw/man-laptop.png">
  </div>
</section>

<section class="projects reveal" id="projects">
  <div class="project-card">
    <img src="https://i.ibb.co/7k9Vb6r/project1.png">
    <div class="content"><h3>Design Agency</h3><p>Creative agency website</p></div>
  </div>
  <div class="project-card">
    <img src="https://i.ibb.co/fGyjFkm/project2.png">
    <div class="content"><h3>E-Commerce</h3><p>Online clothing store</p></div>
  </div>
  <div class="project-card">
    <img src="https://i.ibb.co/7CR7TfD/project3.png">
    <div class="content"><h3>Blog Platform</h3><p>Modern blog website</p></div>
  </div>
</section>

<section class="services reveal" id="services">
<h2>My Services</h2>
<div class="services-list">
  <div class="service-item"><h4>Web Design</h4><p>Modern responsive websites</p></div>
  <div class="service-item"><h4>App Development</h4><p>Web and mobile apps</p></div>
  <div class="service-item"><h4>UI/UX</h4><p>Clean user experience</p></div>
</div>
</section>

<section class="skills reveal">
<h2>My Skills</h2>
<div class="skill"><p>HTML</p><div class="bar"><span class="html"></span></div></div>
<div class="skill"><p>CSS</p><div class="bar"><span class="css"></span></div></div>
<div class="skill"><p>JavaScript</p><div class="bar"><span class="js"></span></div></div>
</section>

<section class="contact reveal" id="contact">
<h2>Contact Me</h2>
<form>
<input type="text" placeholder="Your Name" required>
<input type="email" placeholder="Your Email" required>
<textarea placeholder="Your Message"></textarea>
<button type="submit">Send Message</button>
</form>
</section>

<footer>© 2026 Clarity Portfolio</footer>

<script>
/* Typing effect */
const text="Fatiu";
let index=0;
function typeEffect(){
if(index<text.length){
document.getElementById("typing").textContent+=text.charAt(index);
index++;
setTimeout(typeEffect,150);
}}
typeEffect();

/* Scroll reveal */
function reveal(){
let reveals=document.querySelectorAll(".reveal");
for(let i=0;i<reveals.length;i++){
let windowHeight=window.innerHeight;
let elementTop=reveals[i].getBoundingClientRect().top;
let elementVisible=150;
if(elementTop<windowHeight-elementVisible){
reveals[i].classList.add("active");
}}}
window.addEventListener("scroll",reveal);

/* Mouse glow */
const glow=document.querySelector(".cursor-glow");
document.addEventListener("mousemove",e=>{
glow.style.left=e.clientX+"px";
glow.style.top=e.clientY+"px";
});

/* Smooth scroll for navbar links */
document.querySelectorAll('nav a[href^="#"]').forEach(link => {
  link.addEventListener('click', function(e){
    e.preventDefault();
    const target = document.querySelector(this.getAttribute('href'));
    if(target){target.scrollIntoView({behavior:'smooth'});}
  });
});

/* Hamburger toggle */
const hamburger = document.getElementById('hamburger');
const navLinks = document.getElementById('nav-links');
hamburger.addEventListener('click', () => {
  navLinks.classList.toggle('active');
});
</script>

</body>
</html>

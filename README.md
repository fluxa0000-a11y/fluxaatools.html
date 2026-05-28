<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Fluxaa Tools</title>

<link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700&display=swap" rel="stylesheet">

<style>

*{
margin:0;
padding:0;
box-sizing:border-box;
font-family:'Poppins',sans-serif;
}

html{
scroll-behavior:smooth;
}

body{
background:#050816;
color:white;
overflow-x:hidden;
}

/* NAVBAR */

nav{
width:100%;
padding:18px 8%;
display:flex;
justify-content:space-between;
align-items:center;
position:fixed;
top:0;
z-index:1000;
background:rgba(0,0,0,0.35);
backdrop-filter:blur(12px);
border-bottom:1px solid rgba(255,255,255,0.08);
}

.logo{
font-size:32px;
font-weight:700;
color:#00d9ff;
}

.logo span{
color:white;
}

.nav-links a{
color:white;
text-decoration:none;
margin-left:25px;
transition:0.3s;
font-size:15px;
}

.nav-links a:hover{
color:#00d9ff;
}

/* HERO */

.hero{
min-height:100vh;
display:flex;
align-items:center;
justify-content:center;
text-align:center;
padding:140px 20px 80px;

background:
radial-gradient(circle at top left,#00d9ff22,transparent 30%),
radial-gradient(circle at bottom right,#9333ea33,transparent 30%),
#050816;
}

.hero-content h1{
font-size:75px;
font-weight:700;
line-height:1.1;
}

.hero-content h1 span{
color:#00d9ff;
}

.tagline{
margin-top:18px;
font-size:24px;
color:#94a3b8;
}

.hero-content p{
max-width:760px;
margin:28px auto;
color:#cbd5e1;
line-height:1.9;
font-size:17px;
}

.hero-btn{
display:inline-block;
margin-top:20px;
padding:15px 38px;
background:linear-gradient(90deg,#00d9ff,#9333ea);
border-radius:14px;
color:white;
text-decoration:none;
font-weight:600;
transition:0.3s;
cursor:pointer;
border:none;
}

.hero-btn:hover{
transform:scale(1.05);
}

/* SECTION */

section{
padding:90px 8%;
}

.section-title{
text-align:center;
margin-bottom:55px;
}

.section-title h2{
font-size:46px;
}

.section-title p{
margin-top:12px;
color:#94a3b8;
}

/* TOOLS */

.tools-grid{
display:grid;
grid-template-columns:repeat(auto-fit,minmax(250px,1fr));
gap:25px;
}

.tool-card{
background:rgba(255,255,255,0.05);
border:1px solid rgba(255,255,255,0.08);
border-radius:24px;
padding:32px;
transition:0.4s;
backdrop-filter:blur(12px);
cursor:pointer;
}

.tool-card:hover{
transform:translateY(-10px);
border-color:#00d9ff;
box-shadow:0 0 30px rgba(0,217,255,0.25);
}

.tool-icon{
font-size:48px;
}

.tool-card h3{
margin-top:18px;
font-size:24px;
}

.tool-card p{
margin-top:12px;
color:#cbd5e1;
line-height:1.8;
font-size:15px;
}

.tool-btn{
display:inline-block;
margin-top:20px;
padding:11px 24px;
border-radius:12px;
background:#00d9ff;
color:black;
text-decoration:none;
font-weight:600;
}

/* ABOUT */

.about-box{
max-width:900px;
margin:auto;
text-align:center;
background:rgba(255,255,255,0.04);
padding:45px;
border-radius:24px;
border:1px solid rgba(255,255,255,0.08);
}

.about-box p{
margin-top:18px;
color:#cbd5e1;
line-height:2;
}

/* STAFF */

.staff-grid{
display:grid;
grid-template-columns:repeat(auto-fit,minmax(220px,1fr));
gap:25px;
}

.staff-card{
background:rgba(255,255,255,0.05);
padding:30px;
border-radius:24px;
text-align:center;
border:1px solid rgba(255,255,255,0.08);
transition:0.3s;
cursor:pointer;
}

.staff-card:hover{
transform:translateY(-8px);
border-color:#00d9ff;
}

.staff-avatar{
width:80px;
height:80px;
border-radius:50%;
background:linear-gradient(90deg,#00d9ff,#9333ea);
margin:auto;
}

.staff-card h3{
margin-top:18px;
}

.staff-card p{
margin-top:8px;
color:#94a3b8;
}

/* CONTACT */

.contact-box{
max-width:700px;
margin:auto;
text-align:center;
}

.contact-box p{
margin-top:15px;
color:#cbd5e1;
line-height:1.8;
}

/* TERMS */

.terms-box{
max-width:900px;
margin:auto;
background:rgba(255,255,255,0.04);
padding:45px;
border-radius:24px;
border:1px solid rgba(255,255,255,0.08);
}

.terms-box p{
color:#cbd5e1;
line-height:2;
}

/* FOOTER */

footer{
margin-top:90px;
padding:40px 20px;
text-align:center;
background:#020617;
border-top:1px solid rgba(255,255,255,0.08);
}

footer h2{
color:#00d9ff;
margin-bottom:18px;
font-size:30px;
}

.footer-links{
margin-bottom:20px;
}

.footer-links a{
color:#cbd5e1;
text-decoration:none;
margin:0 12px;
transition:0.3s;
font-size:15px;
}

.footer-links a:hover{
color:#00d9ff;
}

.copyright{
color:#64748b;
font-size:14px;
}

/* POPUP */

.popup{
position:fixed;
top:0;
left:0;
width:100%;
height:100%;
background:rgba(0,0,0,0.7);
display:none;
justify-content:center;
align-items:center;
padding:20px;
z-index:2000;
}

.popup-content{
background:#0f172a;
padding:40px;
border-radius:24px;
max-width:700px;
width:100%;
border:1px solid rgba(255,255,255,0.08);
position:relative;
animation:popup 0.3s ease;
}

@keyframes popup{
from{
transform:scale(0.8);
opacity:0;
}
to{
transform:scale(1);
opacity:1;
}
}

.close-btn{
position:absolute;
right:20px;
top:15px;
font-size:28px;
cursor:pointer;
color:white;
}

.popup-logo{
font-size:70px;
text-align:center;
}

.popup-content h2{
text-align:center;
margin-top:15px;
color:#00d9ff;
}

.popup-content p{
margin-top:18px;
line-height:1.9;
color:#cbd5e1;
}

.popup-content ul{
margin-top:20px;
padding-left:20px;
line-height:2;
color:#cbd5e1;
}

.launch-btn{
display:inline-block;
margin-top:25px;
padding:14px 30px;
background:linear-gradient(90deg,#00d9ff,#9333ea);
border-radius:12px;
text-decoration:none;
color:white;
font-weight:600;
}

/* MOBILE */

@media(max-width:768px){

.hero-content h1{
font-size:48px;
}

.tagline{
font-size:18px;
}

.nav-links{
display:none;
}

section{
padding:70px 6%;
}

}

</style>
</head>

<body>

<nav>

<div class="logo">
Fluxaa<span>.</span>
</div>

<div class="nav-links">
<a href="#home">Home</a>
<a href="#tools">Tools</a>
<a href="#about">About</a>
<a href="#staff">Staff</a>
<a href="#contact">Contact</a>
</div>

</nav>

<section class="hero" id="home">

<div class="hero-content">

<h1>
A Company Of <span>Gen Z's</span>
</h1>

<div class="tagline">
Building Smart Digital Tools For The Future 🚀
</div>

<p>
Fluxaa Tools is a modern digital platform focused on creating powerful online tools for students, creators, developers and the next generation of the internet.
</p>

<button class="hero-btn">
Explore Tools
</button>

</div>

</section>

<section id="tools">

<div class="section-title">
<h2>Popular Tools</h2>
<p>Modern • Fast • Smart</p>
</div>

<div class="tools-grid">

<div class="tool-card" onclick="openPopup()">

<div class="tool-icon">🧮</div>

<h3>Scientific Calculator</h3>

<p>
Advanced scientific calculations with modern interface.
</p>

<div class="tool-btn">
Open Tool
</div>

</div>

</div>

</section>

<section id="about">

<div class="section-title">
<h2>About Fluxaa</h2>
<p>The Future Of Smart Digital Platforms</p>
</div>

<div class="about-box">

<p>
Fluxaa Technologies is a next-generation digital platform created to provide smart, fast and useful online tools for everyone.
</p>

</div>

</section>

<section id="staff">

<div class="section-title">
<h2>Our Staff</h2>
<p>Creative Minds Behind Fluxaa</p>
</div>

<div class="staff-grid">

<div class="staff-card">

<div class="staff-avatar"></div>

<h3>Mr. Vasu</h3>

<p>Founder & Developer</p>

</div>

<div class="staff-card" onclick="openStaff()">

<div class="staff-avatar"></div>

<h3>Fluxaa Staff</h3>

<p>Coder • Editor • Management</p>

</div>

</div>

</section>

<section id="contact">

<div class="section-title">
<h2>Contact Us</h2>
<p>Let's Build The Future Together</p>
</div>

<div class="contact-box">

<p>
For business inquiries, collaborations and support contact the Fluxaa Technologies team.
</p>

<p>
Email: fluxa0000@gmail.com
</p>

</div>

</section>

<section id="terms">

<div class="section-title">
<h2>Terms & Conditions</h2>
<p>Fluxaa Technologies Policies</p>
</div>

<div class="terms-box">

<p>
By using Fluxaa Tools, users agree to use our platform responsibly. Unauthorized copying, abuse of services or harmful activities are strictly prohibited.
</p>

</div>

</section>

<footer>

<h2>Fluxaa Tools</h2>

<div class="footer-links">

<a href="#home">Home</a>
<a href="#tools">Tools</a>
<a href="#about">About</a>
<a href="#staff">Staff</a>
<a href="#contact">Contact</a>

</div>

<p class="copyright">
© 2026 Fluxaa Technologies. All rights reserved.
</p>

</footer>

<!-- TOOL POPUP -->

<div class="popup" id="toolPopup">

<div class="popup-content">

<div class="close-btn" onclick="closePopup()">
×
</div>

<div class="popup-logo">
🧮
</div>

<h2>Scientific Calculator</h2>

<p>
Fluxaa Scientific Calculator is a fast and modern calculator designed for students and professionals.
</p>

<ul>
<li>Scientific Functions</li>
<li>Modern Interface</li>
<li>Fast Calculations</li>
<li>Mobile Friendly</li>
</ul>

<a href="#" class="launch-btn">
Launch Tool
</a>

</div>

</div>

<!-- STAFF POPUP -->

<div class="popup" id="staffPopup">

<div class="popup-content">

<div class="close-btn" onclick="closeStaff()">
×
</div>

<h2>Fluxaa Staff</h2>

<p><b>Coder:</b> Mr. Vasu</p>
<p><b>Editor:</b> Fluxaa Team</p>
<p><b>Designer:</b> Fluxaa Creative Department</p>
<p><b>Management:</b> Fluxaa Technologies</p>

</div>

</div>

<script>

function openPopup(){
document.getElementById("toolPopup").style.display="flex";
}

function closePopup(){
document.getElementById("toolPopup").style.display="none";
}

function openStaff(){
document.getElementById("staffPopup").style.display="flex";
}

function closeStaff(){
document.getElementById("staffPopup").style.display="none";
}

</script>

</body>
</html>

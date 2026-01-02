# Onlineseba
<html lang="en">
<head>
<meta charset="UTF-8">
<title>OnlineSeba.com | Digital Business Services</title>
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<style>
*{
  margin:0;
  padding:0;
  box-sizing:border-box;
  font-family:Arial, Helvetica, sans-serif;
}

body{
  background:#f4f6f8;
  color:#333;
}

header{
  background:#0a58ca;
  color:#fff;
  padding:15px 20px;
  display:flex;
  justify-content:space-between;
  align-items:center;
  position:sticky;
  top:0;
}

header h1{
  font-size:22px;
}

nav a{
  color:#fff;
  margin-left:15px;
  text-decoration:none;
  font-size:15px;
}

nav a:hover{
  text-decoration:underline;
}

.hero{
  padding:80px 20px;
  text-align:center;
  background:linear-gradient(to right,#0a58ca,#0dcaf0);
  color:white;
}

.hero h2{
  font-size:32px;
  margin-bottom:10px;
}

.hero p{
  font-size:18px;
  margin-bottom:20px;
}

.hero button{
  padding:12px 25px;
  font-size:16px;
  border:none;
  border-radius:5px;
  cursor:pointer;
  background:white;
  color:#0a58ca;
}

section{
  padding:60px 20px;
  max-width:1100px;
  margin:auto;
}

section h2{
  text-align:center;
  margin-bottom:30px;
  color:#0a58ca;
}

.services{
  display:grid;
  grid-template-columns:repeat(auto-fit,minmax(220px,1fr));
  gap:20px;
}

.service{
  background:white;
  padding:25px;
  border-radius:8px;
  box-shadow:0 0 10px rgba(0,0,0,0.1);
  text-align:center;
}

.about{
  text-align:center;
  font-size:17px;
  line-height:1.6;
}

.contact{
  text-align:center;
}

.contact input,
.contact textarea{
  width:90%;
  max-width:400px;
  padding:12px;
  margin:8px auto;
  display:block;
  border:1px solid #ccc;
  border-radius:5px;
}

.contact button{
  padding:12px 30px;
  border:none;
  background:#0a58ca;
  color:white;
  border-radius:5px;
  cursor:pointer;
  font-size:16px;
}

#status{
  margin-top:10px;
  font-weight:bold;
}

footer{
  background:#0a58ca;
  color:white;
  text-align:center;
  padding:15px;
  margin-top:40px;
}
</style>
</head>

<body>

<header>
  <h1>OnlineSeba</h1>
  <nav>
    <a href="#home">Home</a>
    <a href="#services">Services</a>
    <a href="#about">About</a>
    <a href="#contact">Contact</a>
  </nav>
</header>

<div id="home" class="hero">
  <h2>All Digital Services in One Place</h2>
  <p>Fast • Secure • Reliable Online Solutions</p>
  <button onclick="goContact()">Get Service</button>
</div>

<section id="services">
  <h2>Our Services</h2>
  <div class="services">
    <div class="service">Web Development</div>
    <div class="service">App Development</div>
    <div class="service">Online Application Support</div>
    <div class="service">Digital Business Solutions</div>
  </div>
</section>

<section id="about">
  <h2>About OnlineSeba</h2>
  <div class="about">
    OnlineSeba.com is a digital service platform designed to help
    individuals and businesses get fast, reliable and professional
    online services from one place.
  </div>
</section>

<section id="contact">
  <h2>Contact Us</h2>
  <div class="contact">
    <input type="text" id="name" placeholder="Your Name">
    <input type="email" id="email" placeholder="Your Email">
    <textarea id="message" placeholder="Your Message"></textarea>
    <button onclick="sendMessage()">Send Message</button>
    <div id="status"></div>
  </div>
</section>

<footer>
  © 2026 OnlineSeba.com | All Rights Reserved
</footer>

<script>
function goContact(){
  document.getElementById("contact")
  .scrollIntoView({behavior:"smooth"});
}

function sendMessage(){
  const name=document.getElementById("name").value;
  const email=document.getElementById("email").value;
  const message=document.getElementById("message").value;
  const status=document.getElementById("status");

  if(name==""||email==""||message==""){
    status.style.color="red";
    status.innerText="Please fill all fields!";
    return;
  }

  status.style.color="green";
  status.innerText="Message sent successfully! (Backend ready)";
}
</script>



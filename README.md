<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Our Tale ❤️</title>

<style>

body{
margin:0;
font-family: Arial, sans-serif;
background:linear-gradient(135deg,#ff9a9e,#fad0c4);
text-align:center;
overflow-x:hidden;
}

header{
padding:40px;
color:white;
}

.story{
max-width:900px;
margin:auto;
background:white;
padding:30px;
border-radius:15px;
box-shadow:0 10px 25px rgba(0,0,0,0.2);
}

.event{
margin:20px 0;
padding:15px;
background:#fff5f7;
border-left:5px solid #ff2d6f;
border-radius:8px;
text-align:left;
}

.date{
color:#ff2d6f;
font-weight:bold;
}

.timer{
font-size:22px;
color:#ff2d6f;
margin:20px 0;
}

button{
padding:12px 25px;
border:none;
background:#ff2d6f;
color:white;
border-radius:8px;
cursor:pointer;
}

button:hover{
background:#ff4b7d;
}

.popup{
display:none;
position:fixed;
top:0;
left:0;
width:100%;
height:100%;
background:rgba(0,0,0,0.6);
}

.popup-content{
background:white;
padding:30px;
border-radius:12px;
max-width:500px;
margin:15% auto;
text-align:left;
}

.close{
float:right;
cursor:pointer;
font-size:20px;
}

.heart{
position:fixed;
color:red;
animation:float 5s linear infinite;
}

@keyframes float{
0%{transform:translateY(0);}
100%{transform:translateY(-100vh);}
}

.star{
position:fixed;
width:2px;
height:2px;
background:white;
animation:fall 5s linear infinite;
}

@keyframes fall{
0%{transform:translateY(-10px);}
100%{transform:translateY(100vh);}
}

</style>
</head>

<body>

<header>
<h1>💖 Our Tale 💖</h1>
<p>A Love Story Written By Destiny</p>
</header>

<div class="story">

<h2>⏳ Our Love Timer</h2>
<div class="timer" id="loveTimer"></div>

<h2>📖 Our Story</h2>

<div class="event">
<span class="date">28 May</span><br>
We met online in a random chat and slowly fell in love.
</div>

<div class="event">
<span class="date">5 June 2025</span><br>
We met in real life for the first time and shared a beautiful moment together.
</div>

<div class="event">
<span class="date">6 June 2025</span><br>
We met again the next day and enjoyed magical moments together.
</div>

<div class="event">
Before leaving we accidentally shared a kiss, a memory we will never forget.
</div>

<div class="event">
After three months we met again and felt the warmth of love once more.
</div>

<br>

<button onclick="openLetter()">Open Secret Love Letter 💌</button>

</div>

<div class="popup" id="letterPopup">
<div class="popup-content">

<span class="close" onclick="closeLetter()">✖</span>

<h2>My Love ❤️</h2>

<p>
It all started on 28 May when two strangers met in a random chat.
Little did we know that moment would become the beginning of our beautiful story.
</p>

<p>
Meeting you on 5 June 2025 felt like destiny.
The moments we shared, the laughter, the unexpected kiss,
all became memories that live in my heart forever.
</p>

<p>
No matter where life takes us,
our tale will always remain special.
Because our story is still being written. ❤️
</p>

</div>
</div>

<audio autoplay loop>
<source src="music.mp3" type="audio/mpeg">
</audio>

<script>

function updateTimer(){
const start = new Date("May 28, 2025 00:00:00");
const now = new Date();
const diff = now - start;

const days = Math.floor(diff/(1000*60*60*24));
const hours = Math.floor((diff%(1000*60*60*24))/(1000*60*60));
const minutes = Math.floor((diff%(1000*60*60))/(1000*60));
const seconds = Math.floor((diff%(1000*60))/1000);

document.getElementById("loveTimer").innerHTML =
days+" days "+hours+" hours "+minutes+" minutes "+seconds+" seconds ❤️";
}

setInterval(updateTimer,1000);

function openLetter(){
document.getElementById("letterPopup").style.display="block";
}

function closeLetter(){
document.getElementById("letterPopup").style.display="none";
}

function createHeart(){
const heart=document.createElement("div");
heart.classList.add("heart");
heart.innerHTML="❤️";
heart.style.left=Math.random()*100+"vw";
heart.style.fontSize=(Math.random()*20+10)+"px";
document.body.appendChild(heart);

setTimeout(()=>{heart.remove();},5000);
}

setInterval(createHeart,400);

function createStar(){
const star=document.createElement("div");
star.classList.add("star");
star.style.left=Math.random()*100+"vw";
document.body.appendChild(star);

setTimeout(()=>{star.remove();},5000);
}

setInterval(createStar,200);

</script>

</body>
</html>
# Cyber03
CyberPunkExe03Real
<!DOCTYPE html>
<html lang="id">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Cyberpunk Music</title>

<style>
*{
margin:0;
padding:0;
box-sizing:border-box;
}

body{
height:100vh;
display:flex;
justify-content:center;
align-items:center;
background:black;
overflow:hidden;
font-family:Arial;
}

/* Background Neon */
body::before{
content:"";
position:absolute;
width:100%;
height:100%;
background:
linear-gradient(90deg,transparent,#00ffff22,transparent),
linear-gradient(transparent,#ff00ff22,transparent);
animation:bg 4s linear infinite;
}

@keyframes bg{
0%{
transform:translateY(-100%);
}
100%{
transform:translateY(100%);
}
}

/* Tombol */
button{
position:relative;
z-index:1;
padding:20px 45px;
font-size:28px;
font-weight:bold;
color:#00ffff;
background:#111;
border:2px solid #00ffff;
border-radius:20px;
cursor:pointer;
box-shadow:
0 0 20px #00ffff,
0 0 40px #00ffff;
transition:0.3s;
}

button:hover{
transform:scale(1.1);
box-shadow:
0 0 40px #00ffff,
0 0 80px #00ffff;
}
</style>
</head>

<body>

<button id="playBtn">
🔊 PLAY MUSIC
</button>

<audio id="music">
<source src="suara.mp3" type="audio/mp3">
</audio>

<script>
const btn = document.getElementById("playBtn");
const music = document.getElementById("music");

btn.addEventListener("click", function(){
music.play().then(() => {
console.log("Musik diputar");
}).catch((error) => {
alert("Suara gagal diputar");
console.log(error);
});
});
</script>

</body>
</html>

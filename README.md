# NURHALIFAIMUT
<!DOCTYPE html>
<html lang="id">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Ajarkan Saya Membuat Game</title>

<style>
*{
    margin:0;
    padding:0;
    box-sizing:border-box;
    font-family:'Poppins',sans-serif;
}

body{
    height:100vh;
    background:linear-gradient(135deg,#ffd6e7,#ffffff);
    display:flex;
    justify-content:center;
    align-items:center;
    overflow:hidden;
}

.container{
    text-align:center;
    background:white;
    padding:35px;
    border-radius:25px;
    box-shadow:0 10px 30px rgba(255,105,180,0.3);
    width:90%;
    max-width:500px;
}

.stickers{
    font-size:55px;
    margin-bottom:15px;
}

h1{
    color:#ff4f9a;
    margin-bottom:10px;
}

p{
    color:#666;
    margin-bottom:25px;
}

.buttons{
    position:relative;
    height:150px;
}

button{
    border:none;
    padding:14px 30px;
    border-radius:50px;
    font-size:18px;
    font-weight:bold;
    cursor:pointer;
    transition:0.3s;
}

#yesBtn{
    background:#ff69b4;
    color:white;
    margin-right:10px;
}

#yesBtn:hover{
    transform:scale(1.08);
}

#noBtn{
    background:white;
    color:#ff69b4;
    border:3px solid #ff69b4;
    position:absolute;
}

#message{
    margin-top:20px;
    font-size:18px;
    color:#ff1493;
    font-weight:bold;
    min-height:50px;
}

.sparkle{
    animation:float 2s infinite ease-in-out;
}

@keyframes float{
    50%{
        transform:translateY(-8px);
    }
}
</style>
</head>

<body>

<div class="container">
    <div class="stickers sparkle">
        🎮 ✨ 💖
    </div>

    <h1>Ajarkan Saya Membuat Game!</h1>

    <p>
        Apakah kamu ingin mulai belajar membuat game hari ini?
    </p>

    <div class="buttons">
        <button id="yesBtn">Iya 💖</button>
        <button id="noBtn">Tidak 😅</button>
    </div>

    <div id="message"></div>
</div>

<script>
const yesBtn = document.getElementById("yesBtn");
const noBtn = document.getElementById("noBtn");
const message = document.getElementById("message");

const pesanPositif = [
    "Hebat! 🎮 Kamu bisa mulai dengan HTML, CSS, dan JavaScript.",
    "Keren! 🚀 Langkah pertama adalah membuat game sederhana seperti Tebak Angka.",
    "Mantap! 🌟 Belajar game development melatih logika dan kreativitas.",
    "Luar biasa! 💖 Setiap game besar dimulai dari proyek kecil.",
    "Semangat! 🎯 Terus berlatih dan kamu bisa membuat game impianmu."
];

yesBtn.addEventListener("click", () => {
    const random =
        pesanPositif[Math.floor(Math.random() * pesanPositif.length)];

    message.innerHTML = random;
});

function moveButton(){
    const maxX = window.innerWidth - noBtn.offsetWidth - 20;
    const maxY = window.innerHeight - noBtn.offsetHeight - 20;

    const x = Math.random() * maxX;
    const y = Math.random() * maxY;

    noBtn.style.left = x + "px";
    noBtn.style.top = y + "px";
}

noBtn.addEventListener("mouseover", moveButton);
noBtn.addEventListener("click", moveButton);
</script>

</body>
</html>

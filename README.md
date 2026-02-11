<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Para Mi Amor ❤️</title>

<style>
body{
    margin:0;
    font-family: Arial, sans-serif;
    background: linear-gradient(45deg,#ff0066,#ff4d94);
    display:flex;
    justify-content:center;
    align-items:center;
    height:100vh;
}

.card{
    background:#f5e6d8;
    width:90%;
    max-width:600px;
    padding:30px;
    border-radius:20px;
    box-shadow:0 10px 30px rgba(0,0,0,0.3);
    text-align:left;
    position:relative;
}

h1{
    text-align:center;
    color:#b30059;
}

.heart-tree{
    text-align:center;
    font-size:60px;
}

.counter{
    margin-top:20px;
    font-weight:bold;
}

.falling{
    position:absolute;
    color:red;
    animation:fall 5s linear infinite;
}

@keyframes fall{
    0%{transform:translateY(-10px);opacity:1;}
    100%{transform:translateY(300px);opacity:0;}
}
</style>
</head>

<body>

<div class="card">
    <h1>Para el amor de mi vida ❤️</h1>

    <p>
        Si pudiera elegir un lugar seguro, sería a tu lado.
    </p>
    <p>
        Cuanto más tiempo estoy contigo más te amo.
    </p>
    <p><strong>— I Love You!</strong></p>

    <div class="heart-tree">🌳❤️</div>

    <div class="counter">
        Mi amor por ti comenzó hace...
        <div id="time"></div>
    </div>
</div>

<script>
const startDate = new Date("2026-01-27T00:00:00"); // CAMBIA ESTA FECHA

function updateCounter(){
    const now = new Date();
    const diff = now - startDate;

    const days = Math.floor(diff / (1000*60*60*24));
    const hours = Math.floor((diff / (1000*60*60)) % 24);
    const minutes = Math.floor((diff / (1000*60)) % 60);
    const seconds = Math.floor((diff / 1000) % 60);

    document.getElementById("time").innerHTML =
        `${days} días ${hours} horas ${minutes} minutos ${seconds} segundos`;
}

setInterval(updateCounter,1000);
updateCounter();

// corazones cayendo
function createHeart(){
    const heart = document.createElement("div");
    heart.classList.add("falling");
    heart.innerHTML="❤️";
    heart.style.left=Math.random()*100+"%";
    heart.style.top="0px";
    document.body.appendChild(heart);

    setTimeout(()=>{heart.remove();},5000);
}
setInterval(createHeart,800);
</script>

</body>
</html>

<!--
**rosariodarlin570-wq/rosariodarlin570-wq** is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile.

Here are some ideas to get you started:

- 🔭 I’m currently working on ...
- 🌱 I’m currently learning ...
- 👯 I’m looking to collaborate on ...
- 🤔 I’m looking for help with ...
- 💬 Ask me about ...
- 📫 How to reach me: ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...
-->

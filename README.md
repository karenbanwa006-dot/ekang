<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>My Valentine 💘</title>

<style>
body {
    margin: 0;
    font-family: 'Segoe UI', sans-serif;
    background: linear-gradient(135deg, blue, skyblue);
    overflow: hidden;
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100vh;
    color: black;
    text-align: center;
}

.container {
    z-index: 2;
}

h1 {
    font-size: 3em;
    margin-bottom: 20px;
}

button {
    padding: 15px 30px;
    font-size: 18px;
    border: none;
    border-radius: 30px;
    background-color: white;
    color: #ff4d6d;
    cursor: pointer;
    transition: 0.3s ease;
}

button:hover {
    background-color: #ffe0e9;
    transform: scale(1.1);
}

#letter {
    display: none;
    margin-top: 20px;
    font-size: 1.3em;
    background: rgba(255, 255, 255, 0.2);
    padding: 20px;
    border-radius: 15px;
    max-width: 400px;
}

/* Floating hearts */
.heart {
    position: absolute;
    bottom: -50px;
    font-size: 20px;
    animation: float 6s linear infinite;
}

@keyframes float {
    0% { transform: translateY(0); opacity: 1; }
    100% { transform: translateY(-110vh); opacity: 0; }
}
</style>
</head>

<body>

<div class="container">
    <h1>HAPPY VALENTINES JAMES MYLOVEEEE😍</h1>
    <button onclick="openLetter()">open my letter 💌</button>
    <div id="letter">
        i know our relationship was unexpected but i hope it
        will last, iloveyouuuu more than anything now, no more kuda na
        basta mahal kita kahit kupal ka iloveyouuuu💋♥️
    </div>
</div>

<script>
function openLetter() {
    document.getElementById("letter").style.display = "block";
}

// Floating hearts generator
function createHeart() {
    const heart = document.createElement("div");
    heart.classList.add("heart");
    heart.innerHTML = "🩵";
    heart.style.left = Math.random() * 100 + "vw";
    heart.style.fontSize = Math.random() * 20 + 15 + "px";
    heart.style.animationDuration = Math.random() * 3 + 3 + "s";
    document.body.appendChild(heart);

    setTimeout(() => {
        heart.remove();
    }, 6000);
}

setInterval(createHeart, 300);
</script>

</body>
</html>

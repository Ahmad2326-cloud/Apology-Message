<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>For You ❤️</title>
<style>
    body {
        font-family: 'Arial', sans-serif;
        background: linear-gradient(135deg, #f9d6d2, #f6f0c4, #d4e9f9);
        height: 100vh;
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        text-align: center;
        margin: 0;
        padding: 20px;
        overflow: hidden;
    }
    h1 {
        font-size: 1.3em;
        color: #444;
        max-width: 90%;
        animation: fadeIn 2s ease forwards;
        line-height: 1.5em;
        z-index: 2;
    }
    button {
        margin-top: 20px;
        padding: 12px 20px;
        background-color: #ff7f7f;
        border: none;
        border-radius: 20px;
        color: white;
        font-size: 1em;
        cursor: pointer;
        transition: 0.3s;
        z-index: 2;
    }
    button:hover {
        background-color: #ff4c4c;
    }
    @keyframes fadeIn {
        0% {opacity: 0; transform: translateY(20px);}
        100% {opacity: 1; transform: translateY(0);}
    }
    .heart {
        position: absolute;
        color: red;
        font-size: 20px;
        animation: float 5s linear infinite;
    }
    @keyframes float {
        0% { transform: translateY(0) scale(1); opacity: 1; }
        100% { transform: translateY(-800px) scale(1.5); opacity: 0; }
    }
</style>
</head>
<body>

<h1 id="message">
I’m really sorry for my overthinking, and I know it sometimes gets in the way of the love we share. I want you to know that I’m working on it because you mean so much to me. I don’t just want to love you, I want to be your safe place — the person you can come to without fear, without hesitation. I want to be the warmth you come home to, the peace you feel when the world gets too loud. You are my heart, and I’ll do everything I can to protect and cherish what we have. ❤️
</h1>
<button id="nextBtn">Click here</button>

<script>
document.getElementById("nextBtn").addEventListener("click", function() {
    document.body.style.background = "linear-gradient(135deg, #ffd1dc, #ffe6f7, #ffb3ba)";
    document.getElementById("message").innerHTML = "I love you ❤️";
    document.getElementById("nextBtn").style.display = "none";

    setInterval(() => {
        let heart = document.createElement("div");
        heart.innerHTML = "❤️";
        heart.classList.add("heart");
        heart.style.left = Math.random() * 100 + "vw";
        heart.style.fontSize = Math.random() * 20 + 20 + "px";
        heart.style.animationDuration = (Math.random() * 2 + 3) + "s";
        document.body.appendChild(heart);
        setTimeout(() => heart.remove(), 5000);
    }, 300);
});
</script>

</body>
</html>

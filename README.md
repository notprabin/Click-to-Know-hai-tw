# Click-to-Know-hai-tw
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>6th Month Anniversary</title>

<link href="https://fonts.googleapis.com/css2?family=Great+Vibes&family=Poppins&display=swap" rel="stylesheet">

<style>
body {
    margin: 0;
    background: maroon;
    font-family: 'Poppins', sans-serif;
    overflow-x: hidden;
}

/* Pages */
.page {
    min-height: 100vh;
    display: none;
    justify-content: center;
    align-items: center;
    text-align: center;
    padding: 20px;
}
.page.active {
    display: flex;
}

/* Card */
.card {
    background: rgba(255,255,255,0.1);
    padding: 30px;
    border-radius: 20px;
    max-width: 500px;
    width: 100%;
    color: white;
}

/* Page 2 love letter */
.letter {
    background: #fff8f0;
    color: #5a1a1a;
    padding: 30px;
    border-radius: 12px;
    max-width: 520px;
    width: 100%;
    text-align: left;
    font-size: 18px;
    line-height: 1.8;
    box-shadow: 0 10px 30px rgba(0,0,0,0.3);
}

.letter h2 {
    text-align: center;
    font-family: 'Great Vibes', cursive;
    font-size: 42px;
    margin-bottom: 20px;
}

.signature {
    margin-top: 30px;
    text-align: right;
    font-family: 'Great Vibes', cursive;
    font-size: 32px;
}

/* Headings */
h1 {
    font-family: 'Great Vibes', cursive;
    font-size: 48px;
}

/* Button */
button {
    margin-top: 20px;
    padding: 12px 30px;
    font-size: 16px;
    border: none;
    border-radius: 25px;
    cursor: pointer;
    background: white;
    color: maroon;
}

/* Hearts animation */
.heart {
    position: fixed;
    bottom: -20px;
    font-size: 20px;
    animation: float 6s linear infinite;
}

@keyframes float {
    from { transform: translateY(0); opacity: 1; }
    to { transform: translateY(-100vh); opacity: 0; }
}
</style>
</head>

<body>

<!-- PAGE 1 -->
<div class="page active" id="page1">
    <div class="card">
        <h1>Happy 6th Month Anniversary ❤️</h1>
        <p>
            Six months of love, memories,<br>
            smiles, and moments that mean everything to me 💕
        </p>
        <button onclick="goNext()">Continue ❤️</button>
    </div>
</div>

<!-- PAGE 2 -->
<div class="page" id="page2">
    <div class="letter">
        <h2>My Love Letter 💌</h2>

        <p>
            I know it’s been hard for us, but I am sure we will continue moving forward.
            Every challenge we face only reminds me how much you mean to me.
        </p>

        <p>
            I love you today, tomorrow, and forever.
            My feelings for you are not just for now — they are for every day that comes next.
        </p>

        <p>
            I want to be the only one for you.
            I want to stand by you, choose you, and love you in every moment,
            no matter what life brings our way.
        </p>

        <div class="signature">
            Forever yours ❤️
        </div>
    </div>
</div>

<script>
function goNext() {
    document.getElementById("page1").classList.remove("active");
    document.getElementById("page2").classList.add("active");
}

// Floating hearts
setInterval(() => {
    const heart = document.createElement("div");
    heart.className = "heart";
    heart.innerHTML = "❤️";
    heart.style.left = Math.random() * 100 + "vw";
    document.body.appendChild(heart);
    setTimeout(() => heart.remove(), 6000);
}, 500);
</script>

</body>
</html>

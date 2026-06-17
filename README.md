<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Truth or Dare 🎲</title>

<style>
*{
    margin:0;
    padding:0;
    box-sizing:border-box;
    font-family:Arial, sans-serif;
}

body{
    height:100vh;
    display:flex;
    justify-content:center;
    align-items:center;
    background:linear-gradient(135deg,#ff416c,#ff4b2b);
}

.container{
    width:90%;
    max-width:500px;
    background:white;
    padding:30px;
    border-radius:20px;
    text-align:center;
    box-shadow:0 10px 25px rgba(0,0,0,.2);
}

h1{
    color:#ff416c;
    margin-bottom:20px;
}

.card{
    min-height:120px;
    display:flex;
    justify-content:center;
    align-items:center;
    padding:20px;
    border-radius:15px;
    background:#f5f5f5;
    font-size:20px;
    margin-bottom:20px;
}

.buttons{
    display:flex;
    gap:10px;
}

button{
    flex:1;
    padding:12px;
    border:none;
    border-radius:10px;
    color:white;
    font-size:18px;
    cursor:pointer;
}

.truth{
    background:#28a745;
}

.dare{
    background:#dc3545;
}

button:hover{
    opacity:0.9;
}
</style>
</head>
<body>

<div class="container">
    <h1>🎲 Truth or Dare 🎲</h1>

    <div class="card" id="card">
        Choose Truth or Dare
    </div>

    <div class="buttons">
        <button class="truth" onclick="showTruth()">Truth</button>
        <button class="dare" onclick="showDare()">Dare</button>
    </div>
</div>

<script>
const truths = [
"What's your biggest fear?",
"Have you ever lied to your best friend?",
"Who was your first crush?",
"What's the most embarrassing thing you've done?",
"If you could change one thing about yourself, what would it be?",
"What's a secret you've never told anyone?",
"Who do you text the most?"
];

const dares = [
"Sing a song for 30 seconds.",
"Do 10 push-ups.",
"Talk in a funny voice for 1 minute.",
"Dance without music for 20 seconds.",
"Send a funny emoji to someone.",
"Act like a cat for 30 seconds.",
"Try to touch your nose with your tongue."
];

function showTruth(){
    const randomTruth =
        truths[Math.floor(Math.random()*truths.length)];

    document.getElementById("card").innerHTML =
        "🟢 TRUTH<br><br>" + randomTruth;
}

function showDare(){
    const randomDare =
        dares[Math.floor(Math.random()*dares.length)];

    document.getElementById("card").innerHTML =
        "🔴 DARE<br><br>" + randomDare;
}
</script>

</body>
</html>

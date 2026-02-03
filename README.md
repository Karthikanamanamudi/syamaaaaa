<!DOCTYPE html>
<html>
<head>
<title>Valentine for Syamaaaaaaaa</title>
<style>
body{
display:flex;
flex-direction:column;
justify-content:center;
align-items:center;
height:100vh;
font-family:Arial, sans-serif;
background: linear-gradient(135deg, #ff758c, #ff7eb3);
color:white;
text-align:center;
}
h1{font-size:30px;}
button{
padding:14px 28px;
font-size:20px;
border:none;
border-radius:8px;
cursor:pointer;
}
.yes-button{background:#2ecc71;color:white;}
.no-button{background:#e74c3c;color:white;margin-left:12px;}
.buttons{margin-top:24px;}
</style>
</head>
<body>

<h1 id="questionText">Syamaaaaaaaa 💕<br>Will you be my Valentine?</h1>

<div class="buttons">
<button class="yes-button" onclick="handleYesClick()">Yes</button>
<button class="no-button" onclick="handleNoClick()">No</button>
</div>

<script>
let messageIndex = 0;
const messages = [
"Are you sure?",
"Really sure?",
"Think again 😏",
"Come on Syama 💖",
"You can't escape 😜"
];

function handleNoClick(){
const noBtn = document.querySelector('.no-button');
const yesBtn = document.querySelector('.yes-button');

noBtn.textContent = messages[messageIndex];
messageIndex = (messageIndex + 1) % messages.length;

const size = parseFloat(getComputedStyle(yesBtn).fontSize);
yesBtn.style.fontSize = (size * 1.4) + "px";
}

function handleYesClick(){
document.getElementById("questionText").textContent =
"You are already my Valentine 💖😍";
document.querySelector('.no-button').disabled = true;
document.querySelector('.no-button').style.opacity = "0.5";
}
</script>

</body>
</html>
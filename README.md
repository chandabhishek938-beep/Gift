#gift
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>For My Love ❤️</title>

<style>
body{
    margin:0;
    font-family: Arial, sans-serif;
    text-align:center;
    background: linear-gradient(to right,#ff758c,#ff7eb3);
    color:white;
    overflow-x:hidden;
}

.container{
    padding-top:80px;
}

h1{
    font-size:45px;
}

button{
    padding:15px 30px;
    font-size:18px;
    border:none;
    border-radius:25px;
    background:white;
    color:#ff4d6d;
    cursor:pointer;
    margin:10px;
}

button:hover{
    background:#ffe6ea;
}

/* Popup */
.popup{
    display:none;
    position:fixed;
    top:50%;
    left:50%;
    transform:translate(-50%,-50%);
    background:white;
    color:#ff4d6d;
    padding:30px;
    border-radius:20px;
    width:300px;
}

/* Hearts animation */
.heart{
    position:fixed;
    bottom:-20px;
    color:white;
    animation: float 5s linear infinite;
}

@keyframes float{
    0%{transform:translateY(0);}
    100%{transform:translateY(-100vh);}
}

img{
    width:200px;
    border-radius:20px;
    margin-top:20px;
}
</style>
</head>

<body>

<div class="container">
    <h1>Hey My Love ❤️</h1>
    <h2>Happy Valentine’s Day</h2>

    <p>You are the best thing in my life.</p>

    <!-- Add her photo here -->
    <img src="yourphoto.jpg" alt="Our Photo">

    <br><br>

    <button onclick="showLetter()">Read Love Letter 💌</button>
    <button onclick="proposal()">Click Surprise ❤️</button>

    <!-- Music -->
    <br><br>
    <audio controls autoplay loop>
        <source src="music.mp3" type="audio/mpeg">
    </audio>
</div>

<!-- Love Letter Popup -->
<div class="popup" id="letter">
    <h3>My Love ❤️</h3>
    <p>
    Thank you for coming into my life.  
    Even though we are far, my heart is always with you.  
    I love you forever.
    </p>
    <button onclick="closeLetter()">Close</button>
</div>

<script>
function showLetter(){
    document.getElementById("letter").style.display="block";
}

function closeLetter(){
    document.getElementById("letter").style.display="none";
}

function proposal(){
    alert("Will You Be My Valentine Forever? ❤️");
}

/* Floating hearts */
setInterval(function(){
    let heart=document.createElement("div");
    heart.className="heart";
    heart.innerHTML="❤️";
    heart.style.left=Math.random()*100+"vw";
    heart.style.fontSize=(Math.random()*20+10)+"px";
    document.body.appendChild(heart);

    setTimeout(()=>{heart.remove();},5000);
},300);
</script>

</body>
</html>

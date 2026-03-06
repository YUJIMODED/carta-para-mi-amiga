<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Para la persona más especial 💖</title>

<style>

body{
    margin:0;
    height:100vh;
    display:flex;
    justify-content:center;
    align-items:center;
    font-family:Arial;
    background:linear-gradient(135deg,#ff9a9e,#fad0c4);
    overflow:hidden;
}

/* corazones flotando */

.corazon{
    position:absolute;
    color:#ff4d6d;
    font-size:20px;
    animation:flotar 6s linear infinite;
}

@keyframes flotar{
    0%{
        transform:translateY(100vh);
        opacity:0;
    }
    50%{
        opacity:1;
    }
    100%{
        transform:translateY(-10vh);
        opacity:0;
    }
}

.card{
    background:white;
    padding:40px;
    border-radius:20px;
    text-align:center;
    box-shadow:0 10px 30px rgba(0,0,0,0.2);
    max-width:320px;
}

button{
    padding:12px 25px;
    border:none;
    border-radius:30px;
    background:#ff4d6d;
    color:white;
    font-size:16px;
    cursor:pointer;
}

button:hover{
    transform:scale(1.05);
}

#mensaje{
    margin-top:20px;
    display:none;
    animation:aparecer 2s;
}

@keyframes aparecer{
    from{opacity:0; transform:translateY(20px);}
    to{opacity:1; transform:translateY(0);}
}

</style>
</head>

<body>

<div class="card">
<h2>Para la chica más preciosa 💖</h2>

<button onclick="mostrar()">Ábreme</button>

<div id="mensaje">
<p>
Hola preciosa ✨  
Solo quería decirte que eres una persona increíble.  
Tu sonrisa ilumina cualquier lugar y tu amistad vale más que mil cosas en el mundo.  

Gracias por existir y por ser tan especial 💕  
</p>

<p><b>Con mucho cariño ❤️</b></p>
</div>

</div>

<script>

function mostrar(){
document.getElementById("mensaje").style.display="block";
}

/* crear corazones flotando */

setInterval(()=>{
let corazon=document.createElement("div");
corazon.className="corazon";
corazon.innerHTML="❤";
corazon.style.left=Math.random()*100+"vw";
corazon.style.fontSize=(Math.random()*20+10)+"px";

document.body.appendChild(corazon);

setTimeout(()=>{
corazon.remove();
},6000);

},400);

</script>

</body>
</html>

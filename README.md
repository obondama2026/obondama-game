<!DOCTYPE html>
<html lang="ja">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width,initial-scale=1.0">

<title>当てろ！⅙お盆玉サバイバル！Ver0.1 夜祭り</title>

<style>

*{
margin:0;
padding:0;
box-sizing:border-box;
font-family:"Hiragino Sans","Yu Gothic",sans-serif;
}

body{
background:linear-gradient(#02142e,#000814);
height:100vh;
overflow:hidden;
color:#fff;
}

.screen{
display:none;
position:absolute;
inset:0;
display:flex;
flex-direction:column;
justify-content:center;
align-items:center;
padding:20px;
text-align:center;
}

.screen.active{
display:flex;
}

h1{
font-size:2.2rem;
color:#ffd54f;
text-shadow:
0 0 10px #ff9800,
0 0 25px #ff9800;
animation:titleGlow 2s infinite;
margin-bottom:20px;
}

.subtitle{
font-size:1rem;
margin-bottom:40px;
opacity:.9;
}

button{
border:none;
border-radius:18px;
padding:16px 28px;
font-size:1.2rem;
font-weight:bold;
cursor:pointer;
transition:.2s;
}

button:active{
transform:scale(.93);
}

#startBtn{
background:#ff9800;
color:#fff;
width:260px;
box-shadow:0 0 20px orange;
animation:float 2s ease-in-out infinite;
}

.stageTitle{
font-size:2rem;
margin-bottom:30px;
color:#ffd54f;
text-shadow:0 0 10px orange;
}

.buttonArea{
display:flex;
gap:20px;
flex-wrap:wrap;
justify-content:center;
}

.choice{
width:90px;
height:90px;
font-size:1.3rem;
color:#fff;
}

.red{background:#e53935;}
.blue{background:#1e88e5;}
.green{background:#43a047;}

.star{
position:absolute;
width:2px;
height:2px;
background:white;
border-radius:50%;
animation:starBlink 3s infinite;
}

.lantern{
position:absolute;
top:15px;
font-size:34px;
animation:swing 2.5s ease-in-out infinite;
transform-origin:top center;
}

@keyframes titleGlow{
0%,100%{
text-shadow:0 0 10px orange;
}
50%{
text-shadow:0 0 30px yellow;
}
}

@keyframes float{
0%,100%{
transform:translateY(0);
}
50%{
transform:translateY(-8px);
}
}

@keyframes swing{
0%,100%{
transform:rotate(-4deg);
}
50%{
transform:rotate(4deg);
}
}

@keyframes starBlink{
0%,100%{
opacity:.2;
transform:scale(.8);
}
50%{
opacity:1;
transform:scale(1.5);
}
}

</style>

</head>
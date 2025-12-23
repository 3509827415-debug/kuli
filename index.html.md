<!DOCTYPE html>  
<html lang="zh-CN">  
<head>  
<meta charset="UTF-8">  
<meta name="viewport" content="width=device-width, initial-scale=1.0, user-scalable=no">  
<title>领取</title>  
<style>  
    * { margin:0; padding:0; }  
    body {  
        width:100vw;  
        height:100vh;  
        overflow:hidden;  
        background:#000;  
    }  
    .page {  
        position:absolute;  
        inset:0;  
        display:none;  
    }  
    .page.active {  
        display:block;  
    }  
    .bg {  
        width:100%;  
        height:100%;  
        object-fit:contain;  
        background:#000;  
    }  
    .tap {  
        position:absolute;  
        inset:0;  
        background:rgba(0,0,0,0);  
        border:none;  
    }  
</style>  
</head>  
  
<body>  
  
<div class="page active" id="page1">  
    <img src="img1.jpg" class="bg">  
    <button class="tap" onclick="goNext()"></button>  
</div>  
  
<div class="page" id="page2">  
    <img src="img2.jpg" class="bg">  
</div>  
  
<audio id="music">  
    <source src="kuli.mp3" type="audio/mpeg">  
</audio>  
  
<script>  
function goNext(){  
    document.getElementById('page1').classList.remove('active');  
    document.getElementById('page2').classList.add('active');  
    document.getElementById('music').play();  
}  
</script>  
  
</body>  
</html>  

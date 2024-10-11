# Panchito
Aquí encontrarás el código fuente de mi trabajo Panchito
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Arte CSS: Panchito</title>
    <link rel="stylesheet" href="panchito.css">
</head>
<body>
    <div class="hotdog">
        <div class="bun top"></div>
        <div class="sausage"></div>
        <div class="bun bottom"></div>
    </div>
    <div class="text">Panchito</div>
</body>
</html>

-------------------------------------------------------------------------------------



CSS:


body {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    height: 100vh;
    background-color: lightblue; 
    margin: 0;
}

.hotdog {
    position: relative;
}

.bun {
    width: 200px;
    height: 50px;
    background-color: #d2b48c; 
    border-radius: 25px; 
    position: relative;
}

.bun.top {
    margin-bottom: -20px; 
}

.bun.bottom {
    margin-top: -20px; 
}

.sausage {
    width: 200px;
    height: 30px;
    background-color: #ff6347; 
    border-radius: 15px; 
    position: relative;
    z-index: 1; 
}


.sausage::before,
.sausage::after {
    content: '';
    display: block;
    width: 180px;
    height: 5px;
    background-color: #ffcc00; 
    position: absolute;
}

.sausage::before {
    top: 5px; 
    left: 10px; 
    border-radius: 5px; 
}

.sausage::after {
    bottom: 5px; 
    left: 10px; 
    border-radius: 5px; 
}

.text {
    margin-top: 20px; 
    font-size: 24px; 
    font-weight: bold;
    color: #333; 
}

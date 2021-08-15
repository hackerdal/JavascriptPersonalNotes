# JavascriptPersonalNotes
My personal notes on basic JavaScript

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Hesap Makinesi</title>
    <style>
        h2{
            font-family: Impact, Haettenschweiler, 'Arial Narrow Bold', sans-serif;
            color: blue;
        }

       
        .input{
            font-family: Impact, Haettenschweiler, 'Arial Narrow Bold', sans-serif;
            background-color: cyan;
            color: darkblue;
            width: 160px;
            height: 50px;
        }
    </style>
</head>
<body>
    <h2 >Hesap Makinesi</h2>
    <div id="container">
        <input type="text" class="input" value=0>
        <input type="text" class="input" value=0>
        
    </div>
    <p></p>
    <div>
        <button id="topla" style="color: red; background-color: black; width: 80px;height: 50px;" onclick = "topla(document.getElementsByClassName('input')[0],document.getElementsByClassName('input')[1]);"><b>+</b></button>
<--Toplama butonu--!>
        <button id="cikar" style="color: red; background-color: black;width: 80px;height: 50px;" onclick = "cikar(document.getElementsByClassName('input')[0],document.getElementsByClassName('input')[1]);"><b>-</b></button>
<--Cikarma butonu--!>
        <button id="carp" style="color: red; background-color: black; width: 80px;height: 50px;" onclick = "carp(document.getElementsByClassName('input')[0],document.getElementsByClassName('input')[1]);"><b>*</b></button>
        <button id="bol" style="color: red; background-color: black; width: 80px;height: 50px;" onclick="bolme(document.getElementsByClassName('input')[0],document.getElementsByClassName('input')[1]);"><b>/</b></button>
    </div>
    <p></p>
    <div id="area"  >
        <textarea id="sonuc" cols="40" rows="1" style="background-color:aliceblue;"></textarea>  
    </div>
    
    <script>
        let a;
        let b;
        //toplama fonksiyonu
        function topla(a,b)
        {
            document.getElementById("area").innerHTML = a.value + " + " + b.value + " = " + (parseInt(a.value) + parseInt(b.value));
        }
        //cikarma fonksiyonu
        function cikar(a,b)
        {
            document.getElementById("area").innerHTML = a.value + " - " + b.value + " = " + (parseInt(a.value) - parseInt(b.value));
        }
        //carpma fonksiyonu
        function carp(a,b)
        {
            document.getElementById("area").innerHTML =  a.value + " * " + b.value + " = " + (parseInt(a.value) * parseInt(b.value));
        }

        function bolme(a,b)
        {
            document.getElementById("area").innerHTML = a.value + " / " + b.value + " = " + (parseInt(a.value) / parseInt(b.value));
        }
    </script>
</body>
</html>

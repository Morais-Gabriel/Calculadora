# Calculadora

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=Chrome">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Calculadora</title>
    <style>
        *{
            margin: 0;
            padding: 0;
        }
        .fundo 
        {
            background-image: linear-gradient(45deg,black,blue);
            height: 100vh;
            color: white;
            font-family: Arial, Helvetica, sans-serif;
            text-align: center;
        }
        .Calculadora
        {
            position: absolute;
            background-color: rgba(0,0,0,0.9);
            top: 50%;
            left: 50%;
            transform: translate(-50%,-50%);
            border-radius: 15px;
            padding: 15px;
         }
         .botao
         {
           width: 50px;
           height: 50px;
           font-size: 25px;
           cursor: pointer;
           background-color: rgb(31,31,31);
           border: none;
           color: white;
           margin: 3px;

         }
         .botao:hover
         {
            background-color: black;
         }
         #Resultado
         {
            width: 207px;
            background-color: white;
            height: 30px;
            margin: 5px;
            font-size: 25px;
            color: black;
            text-align: right;
            padding: 5px;

         }

    </style>
</head>
<body>
   <div class="fundo">
        <h1>Gabriel Morais</h1>
            <div class="Calculadora">
            <h1>Calculadora</h1>
            <p id ="Resultado"> </p>
            <table>
                <tr>
                    <td><button class="botao" onclick="clean()">C</button></td>
                    <td><button class="botao" onclick="back()"><</button></td>
                    <td><button class="botao" onclick="insert('/')">/</button></td>
                    <td><button class="botao" onclick="insert('*')">X</button></td>
                </tr>
                <tr>
                    <td><button class="botao" onclick="insert('7')">7</button></td>
                    <td><button class="botao" onclick="insert('8')">8</button></td>
                    <td><button class="botao" onclick="insert('9')">9</button></td>
                    <td><button class="botao" onclick="insert('-')">-</button></td>
                </tr>
                <tr>
                    <td><button class="botao" onclick="insert('4')">4</button></td>
                    <td><button class="botao" onclick="insert('5')">5</button></td>
                    <td><button class="botao" onclick="insert('6')">6</button></td>
                    <td><button class="botao" onclick="insert('+')">+</button></td>
                </tr>
                <tr>
                    <td><button class="botao" onclick="insert('1')">1</button></td>
                    <td><button class="botao" onclick="insert('2')">2</button></td>
                    <td><button class="botao" onclick="insert('3')">3</button></td>
                    <td rowspan = "2"><button class="botao" style = "height: 106px;" onclick = "calcular()">=</button></td>
                </tr>
                <tr>
                    <td colspan="2"><button class="botao" style="width: 104px;" onclick="insert('0')">0</button></td>
                    <td><button class="botao" onclick="insert('.')">.</button></td>
                    
                </tr>
            </table>
        </div>
   </div>
   <script>
    function insert(num)
    {
        var numero = document.getElementById('Resultado').innerHTML;
        document.getElementById('Resultado').innerHTML = numero + num;
    }   
    function clean()
    {
        document.getElementById('Resultado').innerHTML = "";
    }
    function back()
    {
        var resultado = document.getElementById('Resultado').innerHTML;
        document.getElementById('Resultado').innerHTML = resultado.substring (0, resultado.length -1);
    }
    function calcular()
    {
        var resultado = document.getElementById('Resultado').innerHTML;
        if (Resultado)
        {
            document.getElementById('Resultado').innerHTML = eval(resultado);
        }
        else 
        {
            document.getElementById('Resultado').innerHTML = "Nada...";
        }
    }
   </script>
</body>
</html>

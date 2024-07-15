
```python

<!DOCTYPE calculadora>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Calculadora</title>
    <style>
        *{
            margin: 0;
            padding: 0;
        }
        .fundo {
            background-image: linear-gradient(45deg, black, purple);
            height: 100vh;
            color: white;
            font-family: Arial, "Helvetica Neue", Helvetica, sans-serif;
            text-align: center;
        }
        .calculadora{
            position: absolute;
            background-image: linear-gradient( black, purple);
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            border-radius: 15px;
            padding: 15px;
        }
        .botão {
            width: 40px;
            height: 40px;
            margin: 3px;
            font-size: 25px;
            cursor: pointer;
            background-color: rgb(31, 31, 31);
            border: none;
            color: white;
        }
        .botao:hover{
            background-color: rgb(245, 244, 244);
        }
        #resultado{
            background-color: white;
            width: 200px;
            height: 30px;
            margin: 5px;
            font-size: 25px;
            color: black;
            text-align: right;
        }

    </style>





</head>
<body>
    <div class="fundo"> 
        <h1>@espetacular_sanches</h1>
        <div class="calculadora">
            <h1>Calculadora<h1>
                <p id="resultado"></p>
                <table>
                    <tr>
                        <td><button class="botão"onclick="clean('')">C</button></td>
                        <td><button class="botão"onclick="back('')"><</button></td>
                        <td><button class="botão"onclick="insert('/')">/</button></td>
                        <td><button class="botão"onclick="insert('*')">X</button></td>
                    </tr>
                    <tr>
                        <td><button class="botão"onclick="insert('7')">7</button></td>
                        <td><button class="botão"onclick="insert('8')">8</button></td>
                        <td><button class="botão"onclick="insert('9')">9</button></td>
                        <td><button class="botão"onclick="insert('+')">+</button></td>
                    </tr>
                    <tr>
                        <td><button class="botão"onclick="insert('4')">4</button></td>
                        <td><button class="botão"onclick="insert('5')">5</button></td>
                        <td><button class="botão"onclick="insert('6')">6</button></td>
                        <td><button class="botão"onclick="insert('-')">-</button></td>
                    </tr>
                    <tr>
                        <td><button class="botão"onclick="insert('1')">1</button></td>
                        <td><button class="botão"onclick="insert('2')">2</button></td>
                        <td><button class="botão"onclick="insert('3')">3</button></td>
                        <td rowspan="2"><button class="botão" style="height: 85px;" onclick="calcular('')" >=</button></td>
                    </tr>
                    <tr>
                        <td colspan="2"><button class="botão" style="width: 90px;"onclick="insert('0')">0</button></td>
                        <td><button class="botão"onclick="insert('.')">.</button></td>
                    </tr>
                </table>



        </div>
    </div>
    <script>
        function insert(num)
        {
            var numero = document.getElementById('resultado').innerHTML;
            document.getElementById('resultado').innerHTML = numero + num;
        }
        function clean()
        {
            document.getElementById('resultado').innerHTML = "";
        }
        function back()
        {
            var resultado = document.getElementById('resultado').innerHTML;
            document.getElementById('resultado').innerHTML = resultado.substring(0, resultado.length -1);
        }
        function calcular()
        {

            var resultado = document.getElementById('resultado').innerHTML;
            if (resultado){
                document.getElementById('resultado').innerHTML = eval(resultado);

            }
            else
            {
            document.getElementById('resultado').innerHTML = "Nada..."

            }
            
        }
    


    </script>
</body>
</html>

```python

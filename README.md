revisao
body{
    background-color: lightblue; /* Define cor de fundo*/
    color: navy; /* Define cor do texto dos paragráfos*/
    text-shadow: black; /* Adiciona uma sombra ao texto*/
    
    font-family: Arial, Helvetica, sans-serif; /* Define a fonte das letras*/
    font-size: 32px; /* Define o tamanho do texto dos paragráfos*/

    padding: 10%; /* Define o espaço entre o conteúdo de um elemento e sua borda*/
    margin: 5px; /* Define o espaço entre os elementos*/
    
    border: 5px; /* Define a borda de um elemento*/
    border-radius: 50px; /* Define o raio da borda arrendondada de um elemento*/

    width: 50px; /* Define a largura de um elemento*/
    height: 50px; /* Define a altura de um elemento*/
    
    justify-content: center; /* Alinha e destribui os itens horizontalmente*/
    align-items: center; /* Alinha e destribui os itens verticalemente*/
    text-align: center; /* Define o alinhamento horizontal do texto de um elemento*/



}

///////////////////////////////////////////////////////////////////////////////////////////////////

<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>REVISÃO</title>
    <link rel="stylesheet" href="revisão.css">
</head>
<body>
    
    <h1>Título</h1>
    <!-- <h1> insere um título -->
    
    <p>PARAGRÁFO</p>            
    <!-- <p> insere um paragráfo --> 
    
    <p>Imagem</p>
        <img src="cavalo.jpg" height="100px" width="100px">          
    <!-- <img> insere uma imagem -->
    
    <a href="pagina2.html"></a>
    <!-- <a href=""> transfere para outra página -->
    
    <p></p>

    <p>Botão</p>
        <button type="button" id="button1">BOTÃO</button> <!-- <button> cria um botão -->

    <ul>
        <p>Lista não Ordenada</p>
        <li>1</li> 
        <li>2</li>
        <!-- cada item representa um <li> -->
    </ul>
    <!-- <ul> cria uma lista não ordenada -->

    <ol>
        <p>Lista Ordenada</p>
        <li>10</li> 
        <li>20</li>
        <!-- cada item representa um <li> -->
    </ol>
    <!-- <ol> cria uma lista ordenada -->

    <p>Tabela</p>
    <table>
        <tr> 
            <td>1</td>  <!-- <td> coloca o dado em linha-->
            <td>2</td>
            <td>3</td>
        <tr>
            <td>4</td>
            <th>5</th> <!-- <th> deixa a informação em negrito -->
            <td>6</td>
        <tr>
            <td>7</td>
            <td>8</td>
            <td>9</td>
        <tr>
            <td></td>
            <td>0</td>
        
        </tr>
        <!-- <tr> cria espaços para apresentar as informações, também pula linhas-->
    </table>
    <!-- <table> cria uma tabela -->

    <p>Formulário</p>
    <form>
        <label for="text">Insira um nome:</label>
        <input type="text" id="nome" required>
        <br>
        <label for="text">Insira um email:</label>
        <input type="email" id="email" required>
    </form>
    <!-- <form> define um formulário para coletar informações -->

    <select name="selecao" id="texto">
        <option value="select1">1</option>  <!-- <option> define uma opção -->
        <option value="select2">2</option>
        <option value="select3">3</option>
    </select>
    <!-- <select> define uma lista para selecionar alguma opção -->

        <script>
            alert("Meu primeiro JavaScript"); // alert adiciona uma mensagem em pop-up
            var nome= prompt("Qual é seu nome? "); // prompt recolhe uma informação
            alert("Olá " + nome);
            var numero = prompt("Informe o valor do número: ");
            
            var quadrado = numero ** 2;
            alert("O quadrado do número é: " + quadrado);
            
            var preco = Number(prompt("Informe o preço do produto: R$ "));
            var valorAVista = preco * 0.80;
            var valorAPrazo = preco / 3;

            alert("Valor do produto R$: " + 
            preco.toFixed(2) + "\nTotal à vista R$: " + valorAVista.toFixed(2) // toFixed() reduz o número de casa de um número
            + "\nTotal a prazo R$: "+ valorAPrazo.toFixed(2)); 

            function somar(a,b){    // function define uma função
                return a + b;
            }
            let resultado = somar(3,5);
            prompt("A soma é: " + resultado);

            var dobro = function(a){ // function anônima
                return a * 2;
            }
            var num= Number(prompt("Número: "));
            alert("O dobro é: " + dobro(num));

            function situacaoAluno(nota,media){
                var situacao = (nota >= media) ? "Aprovado" : "Reprovado"; // ? seria um IF, : seria um se não
                return situacao;
            }


            
        </script>
        <!-- <script> tranfere para o JavaScript-->

</body>
</html>

///////////////////////////////////////////////////////////////////////////////////////////////////////////

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>CALCULADORA</title>
    <link rel="stylesheet" href="calculadora.css">
</head>
<body>
    <div class="calculadora">
        <h3>CALCULADORA</h3>
        <input type="text" id="tela" readonly>
        <div class="botoes">
            <button onclick="botaotela('1')">1</button>
            <button onclick="botaotela('2')">2</button>
            <button onclick="botaotela('3')">3</button>
            <button onclick="botaotela('+')">+</button>

            <button onclick="botaotela('4')">4</button>
            <button onclick="botaotela('5')">5</button>
            <button onclick="botaotela('6')">6</button>
            <button onclick="botaotela('-')">-</button>

            <button onclick="botaotela('7')">7</button>
            <button onclick="botaotela('8')">8</button>
            <button onclick="botaotela('9')">9</button>
            <button onclick="botaotela('*')">*</button>

            <button onclick="limpartela()">C</button>
            <button onclick="botaotela('0')">0</button>
            <button onclick="calcular()">=</button>
            <button onclick="botaotela('/')">/</button>
           
        </div>
    </div>

    <script>
        function botaotela(value){
            document.getElementById("tela").value += value;
        }

        function limpartela(){
            document.getElementById("tela").value = "";
        }

        function calcular(){
            try{
                var resultado = eval(document.getElementById("tela").value);
                document.getElementById("tela").value = resultado
            } catch (error){
                document.getElementById("tela").value = "Erro!";
            }
        }
    </script>

</body>
</html>

css
body{
    justify-content: center;
    align-items: center;
    display: flex;
    background-color: bisque;
}

.calculadora{
    margin: 50px auto;
    width: 200px;
    background-color: white;
    border-radius: 10px;
}

button{
    padding: 10px;
    margin: 5px;
    font-size: 18px;
    width: 30px;
    height: 30px;
    align-items: center;
    justify-content: center;
}

//////////////////////////////////////////////////////////////////////////////////////

<!DOCTYPE html>
<html lang="pt-br">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>formulario</title>
    <link rel="stylesheet" href="formulario.css">
</head>

<body>
    <div class="formulario">
        <h1>FORMULÁRIO</h1>
        <p>Insira um nome:</p>
        <input type="text" id="nome" required>

        <p>Insira o E-Mail:</p>
        <input type="email" id="email" required>

        <p>Insira o RA:</p>
        <input type="number" id="RA" required>
        <br>

        <select name="select" id="select">
            <option value="estudante">Estudante</option>
            <option value="professor">Professor</option>
            <option value="funcionário">Funcionário</option>
        </select>
        <br>
        <br>
        <div id="botaozin">
            <input type="checkbox">
            <h5>Aceito os termos e condições</h5>
        </div>

        <div id="confirmar">
            <input type="submit" name="confimar" id="confirmar" value="CONFIRMAR">
        </div>
    </div>

</body>

</html>

css
body{
    background-color:bisque;
    font-family: Arial, Helvetica, sans-serif;
    font-size:large;
    text-shadow: black;
    
    margin: 0;
    padding: 10px;

    width: auto;
    height: auto ;
    
    display: flex;
    align-items: center;
    justify-content: center;
}

.formulario{
    background-color: white;
    text-align: left;
    border-radius: 10px;
}

#confirmar{
    color: blue;
    justify-content: center;
    align-content: center;
    align-items: center;
    
}






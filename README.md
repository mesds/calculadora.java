# calculadora.java
Antes de tudo, quero informar que provavelmente não atenderá muito do qual é o projeto necessário. Pois fiz pelo celular e estudei por conta própria para me auto inserir no meio da tecnologia. Mas ao me inscrever, não quis simplesmente desistir do desafio de programação da Cap por parecer incapaz e faltar recursos, logo, aqui está:

Me recusei a perder a oportunidade que vi na Academia, embora provavelmente não atenda muitas das questões e também não tenha as necessárias qualificações. 

 
<head>
   <title>Devin - Calculadora Simples</title

<style type="text/css">
<!--
/* Conteúdo do CSS */
-->
</style>

<script type="text/javascript">
<!--
/* Conteúdo do JavaScript */
-->
</script>

</head>
<body>

<form name="calcform" method="post" action="">
   <fieldset>
      <legend>Devin - Calculadora Simples</legend>

      <label for="valor1">Digite o valor <strong>1</strong>:</label>
      <input type="text" name="valor1" id="valor1" />

      <label for="valor2">Digite o valor <strong>2</strong>:</label>
      <input type="text" name="valor2" id="valor2" />

      <label for="oper">Selecione a operação:</label>
      <select name="oper" id="oper">
         <option value="somar">Somar</option>
         <option value="subtrair">Subtrair</option>
         <option value="multiplicar">Multiplifcar</option>
         <option value="dividir">Dividir</option>
      </select>

      <label for="res">Resultado:</label>
      <input type="text" name="res" id="res" />

      <input type="button" value="Calcular" class="botao" onClick="calcular(document.calcform.oper.value)"/>
   </fieldset>
</form>

form fieldset {
   margin: 10px auto 10px auto;
   width: 40%;
   border: solid black 1px;
   padding: 3%;
}

form legend {
   padding: 6px;
   margin: 10px;
   border: solid black 1px;
   font-size: 90%;
   font-weight: bold;
   background-color: #e8e8e8;
}

form label {
   display: block;
   font-size: 11px;
}

form input {
   width: 100%;
   border: solid #ccc 1px;
   font-size: 11px;
   margin-bottom: 10px;
}

form input.botao {
   display: block;
   width: auto;
   float: right;
}

function calcular(oper) {
   var valor1 = document.calcform.valor1.value;
   var valor2 = document.calcform.valor2.value;

   if (oper == "somar") {
      var res = parseInt(valor1) + parseInt(valor2);
   } else {
      if (oper == "subtrair") {
         var res = valor1-valor2;
      } else {
         if (oper == "multiplicar") {
            var res = valor1*valor2;
         } else {
            var res = valor1/valor2;
         }
      }
   }

   document.calcform.res.value = res;
}

<head>
   <title>Devin - Calculadora Complexa</title>

<style type="text/css">
<!--
/* Conteúdo do CSS */
-->
</style>

<script type="text/javascript">
<!--
/* Conteúdo do JavaScript */
-->
</script>

</head>
<body>

<form name="calcform" method="post" action="">
   <fieldset>
      <legend>Devin - Calculadora Complexa</legend>

      <input type="text" name="visor" id="visor" />

      <table id="calc">
         <tr>
            <td><input type="button" name="num9" class="num" value="9" onclick="calcNum(9)" /></td>
            <td><input type="button" name="num8" class="num" value="8" onclick="calcNum(8)" /></td>
            <td><input type="button" name="num7" class="num" value="7" onclick="calcNum(7)" /></td>
            <td><input type="button" name="somar" class="oper" value="+" onclick="calcParse('somar')" /></td>
         </tr>
         <tr>
            <td><input type="button" name="num6" class="num" value="6" onclick="calcNum(6)" /></td>
            <td><input type="button" name="num5" class="num" value="5" onclick="calcNum(5)" /></td>
            <td><input type="button" name="num4" class="num" value="4" onclick="calcNum(4)" /></td>
            <td><input type="button" name="subtrair" class="oper" value="-" onclick="calcParse('subtrair')" /></td>
         </tr>
         <tr>
            <td><input type="button" name="num3" class="num" value="3" onclick="calcNum(3)" /></td>
            <td><input type="button" name="num2" class="num" value="2" onclick="calcNum(2)" /></td>
            <td><input type="button" name="num1" class="num" value="1" onclick="calcNum(1)" /></td>
            <td><input type="button" name="multiplicar" class="oper" value="*" onclick="calcParse('multiplicar')" /></td>
         </tr>
         <tr>
            <td><input type="button" name="num0" class="num" value="0" onclick="calcNum(0)" /></td>
            <td><input type="button" name="igual" class="num" value="=" onclick="calcParse('resultado')" /></td>
            <td><input type="button" name="limpar" class="num" value="AC" onclick="calcLimpar()" /></td>
            <td><input type="button" name="dividir" class="oper" value="/" onclick="calcParse('dividir')" /></td>
         </tr>
      </table>
   </fieldset>
</form>

</body>
</html>



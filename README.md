# PROJETOS COM VALIDACOES

## VALIDAÇÃO DE CPF 

  Códigos:
  
   - HTML:  

![](img/cpfHtml.png)

 - JS:  




- CSS:

  html, body{
    padding: 0;
    height: 100%;
 
}
body{
    font-family: 'Lucida Sans', 'Lucida Sans Regular', 'Lucida Grande', 'Lucida Sans Unicode', Geneva, Verdana, sans-serif;
    display: flex;
    background-color: rgba(192, 150, 241, 0.938);
}
 
.container{
    display: flex;
    justify-content: center;
    align-items: center;
    width: 100%;
    height: 100%;
}
 
.form{
    background-color: rgb(232, 232, 232);
    padding: 30px;
    border-radius: 20px;
    box-shadow: 0 0 10px black;
    display: flex;
    flex-direction: column;
}
button{
    margin-top: 30px;
    border: none;
    background-color: rgb(187, 96, 247);
    border-radius: 8px;
    padding: 15px;
}
input#cpf{
    height: 30px;
    border-radius: 8px;
    border: none;
}

### EXPLICAÇÃO JS

  A validação foi feita dígito por dígito usando o laço de iteração e repetição "for" para compor um array para cada dígito. Também foi usado "if else" para a confirmação da soma no código.

  ## VALIDAÇÃO DE EMAIL

  Códigos:
  
  - HTML:
      <DOCTYPE html>
<html>
<head>
    <meta charset='utf-8'>
    <meta http-equiv='X-UA-Compatible' content='IE=edge'>
    <title><validaçao de email></title>
    <meta name='viewport' content='width=device-width, initial-scale=1'>
   
   
</head>
<body>
    <form action= "">
        <label>E-mail:</label>
        <input type="text" id ="email user" name="email" onblur="checarEmail()">
        <input type="submit"volue="validar"
        onclick="checarEmail()">
    </form>
 
    <p id="email"></p>
 
    <script src='email.js'></script>
</body>
</html>

 - JS:

    // CODIGO DE VALIDAÇÃO DE EMAIL
//-------------------------------------------------------------------------------------------
function checarEmail(){
    if(document.forms[0].email.value == "" ||
     document.forms[0].email.value.indexOf('@') == -1||
      document.forms[0].email.value.indexOf('.') == -1 ){
        alert("porfavor, informe um e-mail valido");}else{
           // alert("EMAIL INFORMADO COM SUCESSO")
        }
     
}

### EXPLICAÇÃO JS

   Foi usado "if else" para a validação. Se o email informado não tiver '@' e '.com', a tela de alert aparece com a seguinte mensagem "por favor, informe um email válido" pois o email não será válido. Caso o email for válido a tela de alert aparece "email informado com sucesso".


 




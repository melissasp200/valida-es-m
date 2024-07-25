# validacoes-m

## VALIDAÇÃO DE CPF 

  Códigos:
     - HTML:
       
       <!DOCTYPE html>
<html>
<head>
    <meta charset='utf-8'>
    <meta http-equiv='X-UA-Compatible' content='IE=edge'>
    <title>validação de CPF</title>
    <meta name='viewport' content='width=device-width, initial-scale=1'>
    <link rel='stylesheet' type='text/css' media='screen' href='cpf.css'>
</head>
<body>
    <!-- maxlength limita a quantidade de numeros que pode ficar no campo-->
 
    <form action="" id="cpfForm">
        <label for="">CPF:</label>
        <input type="text" id="cpf" name="cpf" maxlength="14">
        <button type="submit">VALIDAR</button>
    </form>
   
    <p id="message"></p>
 
    <p id="cpf"></p>
   
    <script src='cpf.js'></script>
</body>

      
</html>



 - JS:
     // VALIDAÇÃO DE CPF DIRETO NO JAVASCRIPT
 
// Adicionando escutador ao formulário
document.getElementById('cpfForm').addEventListener('submit', function(event){
    event.preventDefault();
 
    const cpf = document.getElementById('cpf').value;
    const msg = document.getElementById('message');
 
    if(validarCPF(cpf)){
        msg.textContent = 'O CPF é válido!';
        msg.style.color = 'green';
    }else{
        msg.textContent = 'O CPF é inválido!';
        msg.style.color = 'red';
    }
}
);
 
function validarCPF(cpf){
    cpf = cpf.replace(/[^\d]+/g, ''); // Remove caracteres não numéricos
 
    // Estrutura de decisão para verificar quantidade de dígitos e se todos os digitos são iguais
    if(cpf.length !== 11 || /^(\d)\1{10}$/.test(cpf)){
        return false;
    }
   
    let soma = 0;
    let resto;
 
    // Validando 10º digito do CPF - o primeiro digito verificador
    for(let i=1;i <= 9;i++){
        soma += parseInt(cpf.substring(i-1, i)) * (11 - i);
    }
 
    resto = (soma * 10) % 11;
 
    if((resto === 10) || (resto === 11)){
        resto = 0;
    }
    if(resto !== parseInt(cpf.substring(9, 10))){
        return false;
    }
    // Validando 11º digito do CPF - o segundo digito verificador
    soma = 0;
    for(let i = 1; i <= 10; i++){
        soma += parseInt(cpf.substring(i-1, i)) * (12 - i);
    }
 
    resto = (soma * 10) % 11;
 
    if((resto === 10) || (resto === 11)){
        resto = 0;
    }
   
    if(resto !== parseInt(cpf.substring(10, 11))){
        return false;
    }
 
    return true;
}


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

## EXPLICAÇÃO JS

  A validação foi feita dígito por dígito usando o laço de iteração e repetição "for" para compor um array para cada dígito. Também foi usado "if else" para a confirmação da soma no código.

  ## VALIDAÇÃO DE EMAIL

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




 




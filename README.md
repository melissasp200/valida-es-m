# validacoes-m

- VALIDAÇÃO DE CPF 

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
 




#### Desafio 2 Ex-4 Atividade segundo Bimestre.
---
*Crie dois arquivos PHP:
O primeiro deve conter um formulário com dois campos: login, password
Ao se submeter no formulário, deve ser gravado na sessao do PHP esse login e password.*
*O segundo arquivo deve capturar da sessao o login e o password (se existir)
Pode ser listado os valores com o print_r*
login.php
~~~~php
<?php
    session_start();

    if($_POST){
        $login = $_POST['login'] ?? null;
        $senha = $_POST['senha'] ?? null;

        if (isset($login) && isset($senha)) {
            $_SESSION['login'] = $login;
            $_SESSION['senha'] = $senha;
    
            echo "<script>location.href='index.php'</script>";
        }

    }


?>


<div>
    <form method="POST" style="text-align: center;">
        <label for="login">Login</label>
        <input type="text" id="login" name="login" placeholder="login">
        <label for="senha">Senha</label>
        <input type="password" id="senha" name="senha" placeholder="senha">
        <button type="submit">Efetuar login</button>
    </form> 
</div>
~~~~
---



index.php
~~~~php
<?php
    session_start();
?>

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Trabalho</title>
</head>
<body>
    <h1>Informaçoes do login</h1>
    <?php
        echo "Login: " . $_SESSION['login'] . "<br>";
        echo "Senha: " . $_SESSION['senha'] . "<br>";
    ?>
    <a href="login.php">Voltar</a>
</body>
</html>
~~~~
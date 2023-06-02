## Dentro do index.php:
~~~php
<?php session_start() ?>

<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" href="./css/style.css">
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-9ndCyUaIbzAi2FUVXJi0CjmCapSmO7SnpJef0486qhLnuZ2cdeRhO02iuK6FUUVM" crossorigin="anonymous">
    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/js/bootstrap.bundle.min.js" integrity="sha384-geWF76RCwLtnZ8qwWowPQNguL3RmwHVBC9FhGdlKrxdiJJigb/j/68SIy3Te4Bkz" crossorigin="anonymous"></script>
    <title>Login</title>
</head>
<body>
    <div class="container text-center">
        <h1>Bem vindo a Sessao</h1>
        <table class="table table-dark table-striped">
            <thead>
                <tr>
                <th scope="col">Nome</th>
                <th scope="col">Senha</th>
                </tr>
            </thead>
            <tbody>
                <tr>
                <td>
                    <?= $_SESSION["sessao"]["login"]?>
                </td>
                <td>
                    <?= $_SESSION["sessao"]["senha"]?>
                </td>
                </tr>
            </tbody>
        </table>
    </div>
</body>
</html>
~~~

## Dentro do login.php:
~~~php
<?php
    session_start();

    if($_POST){
        $nome = $_POST["login"];
        $senha = $_POST["senha"];

        if($nome && $senha){
            $_SESSION["sessao"] = array("login" => $nome, "senha" => $senha);
        }

        echo "<script>location.href='index.php' </script>";
    }

?>
<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" href="./css/style.css">
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-9ndCyUaIbzAi2FUVXJi0CjmCapSmO7SnpJef0486qhLnuZ2cdeRhO02iuK6FUUVM" crossorigin="anonymous">
    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/js/bootstrap.bundle.min.js" integrity="sha384-geWF76RCwLtnZ8qwWowPQNguL3RmwHVBC9FhGdlKrxdiJJigb/j/68SIy3Te4Bkz" crossorigin="anonymous"></script>
    <title>Login</title>
</head>
<div class="center">
    <h1>Login</h1>
    <form method="POST">
        <div class="txt_field">
            <input type="text" name="login" required>
            <span></span>
            <label>Username</label>
        </div>
        <div class="txt_field">
            <input type="password" name="senha" required>
            <span></span>
            <label>password</label>
        </div>
            <input type="submit" name="acao" value="Login">
    </form>
</div>
~~~
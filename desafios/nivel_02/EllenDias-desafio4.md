# Desafio 4
## Formulário

```php
    session_start();

    if($_POST){
        $login = $_POST['login'] ?? NULL;
        $senha = $_POST['senha'] ?? NULL;
    
       $_SESSION['usuario'] = array(
        'login' => $login,
        'senha' => $senha,
    );
    echo "<script>window.location.href='cadastro.php'</script>";
}
?>
<!doctype html>
<html lang="pt-BR">
  <head>
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width, initial-scale=1">
    <title>Formulário</title>
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0-alpha3/dist/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-KK94CHFLLe+nY2dmCWGMq91rCGa5gtU4mk92HdvYe+M/SXH301p5ILy+dN9+nJOZ" crossorigin="anonymous">
    <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/bootstrap-icons@1.10.5/font/bootstrap-icons.css">
    <link rel="stylesheet" href="style.css">
    </head>
  <body>
        <form method="POST">
            <h2>Formulario</h2>
                <div class="form-group">Login
                    <input class="form-control" type="text" name="login">
                <div class="form-group">Senha
                    <input class="form-control" type="password" name="senha" >
                <div class="form-group">
                    <button class="btn btn-primary btn-block" type="submit">Cadastrar</button>
                </div>
        </form>
  </body>
</html>
```

## Cadastro
```php
<?php
session_start();
  $login = $_SESSION['usuario']['login'];
  $senha = $_SESSION['usuario']['senha'];
    echo "$login <br> $senha";
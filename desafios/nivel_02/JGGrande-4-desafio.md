# Para o desafio proposto temos o seguinte código 

## index.php
~~~php
<?php
if($_POST){
    $login = $_POST['login'] ?? NULL;
    $senha = $_POST['password'] ?? NULL;
    if(!empty($login) and !empty($senha)){
        session_start();

        $_SESSION['login'] = $login;
        $_SESSION['senha'] = $senha;
        
        echo"<script>window.location.href='mostrar.php'</script>";
    }
}

?>
<!DOCTYPE html>
<html>
	<head>
		<meta http-equiv="Content-Type" content="text/html; charset=UTF-8" />
		<meta http-equiv="pragma" content="no-cache" />
		<meta http-equiv="expires" content="-1" />
		<title>Login - Rede Wi-Fi</title>
		<link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0-alpha3/dist/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-KK94CHFLLe+nY2dmCWGMq91rCGa5gtU4mk92HdvYe+M/SXH301p5ILy+dN9+nJOZ" crossorigin="anonymous">

	</head>
	<body>

	<div class="bg-light" style="width:500px;margin:auto;margin-top:100px;text-align: center;">
			<div class="well well-large">
				<img src="https://i.ibb.co/3snLP1K/logo.png" alt="Wi-Fi Grupo ALFA" title="Wi-Fi Grupo ALFA">
				<h3>Acesso ao Wi-Fi</h3>
				<form method="post" action="" class="form-inline">
					<label for="username">Login:</label>
					<input type="text" name="login" id="login" value="" placeholder="Digite seu RA" class="input-medium" required style="height:30px;">
					<label for="password">Senha:</label>
					<input type="password" name="password" id="password" placeholder="Digite sua Senha" class="input-medium" required style="height:30px;">
					<input type="submit" class="btn btn-success" value="Entrar">
				</form>
				<p>O login para acesso a rede sem fio da UniALFA é seu RA (número de registro acadêmico) e a senha para primeiro acesso é o próprio RA novamente. No primeiro acesso o sistema solicitará a troca de senha.<br>
					Caso tenha problemas, por favor, procure o Técnico de Informática na Sala de TI.
				</p>
			</div>
		</div>
        <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0-alpha3/dist/js/bootstrap.bundle.min.js" integrity="sha384-ENjdO4Dr2bkBIFxQpeoTz1HIcje39Wm4jDKdf19U8gI4ddQ3GYNS7NTKfAdVQSZe" crossorigin="anonymous"></script>
	</body>
</html>
~~~

## cadastro.php

~~~php
<?php
    session_start();
    $login = $_SESSION["login"] ?? NULL;
    $senha = $_SESSION["senha"] ?? NULL;
?>

<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Mostrar</title>
</head>
<body style="background-color: #556270;">

<div style="text-align: center;margin-top: 15%; font-family: Arial">
    <h1>Login: <?=$login?></h1>
    <h1>Senha: <?=$senha?></h1>
</div>


</body>
</html>
~~~

# Tendo o seguinte resultado
<img src="https://i.ibb.co/0C4L1mT/Captura-de-Tela-2023-05-24-a-s-21-38-48.png" alt="Captura-de-Tela-2023-05-24-a-s-21-38-48" border="0">

<img src="https://i.ibb.co/QvgfQ1R/Captura-de-Tela-2023-05-24-a-s-21-42-18.png" alt="Captura-de-Tela-2023-05-24-a-s-21-42-18" border="0">

## Agora vamos em partes

### Primeiro criamos um html basico com um formulario POST

~~~php

<form method="post" action="" class="form-inline">
	<label for="username">Login:</label>
	    <input type="text" name="login" id="login" value="" placeholder="Digite seu RA" class="input-medium" required style="height:30px;">
		<label for="password">Senha:</label>
		<input type="password" name="password" id="password" placeholder="Digite sua Senha" class="input-medium" required style="height:30px;">
		<input type="submit" class="btn btn-success" value="Entrar">
</form>


~~~

### O formulario manda para o proprio arquivo ao ser submetido assim podemos pegar os dados verificando se existe uma requisição POST com $_POST

~~~php
if($_POST){
    $login = $_POST['login'] ?? NULL;
    $senha = $_POST['password'] ?? NULL;
    if(!empty($login) and !empty($senha)){
    }
}
~~~

### agora podemos salvar os dados na sessão atual e redirecionar para a pagina mostrar.php

~~~php
if($_POST){
    $login = $_POST['login'] ?? NULL;
    $senha = $_POST['password'] ?? NULL;
    if(!empty($login) and !empty($senha)){
        session_start();

        $_SESSION['login'] = $login;
        $_SESSION['senha'] = $senha;
        
        echo"<script>window.location.href='mostrar.php'</script>";
    }
}
~~~

### Agora dentro da pagina mostrar.php pegamos as informações de dentro da seção

~~~php
<?php
    session_start();
    $login = $_SESSION["login"] ?? NULL;
    $senha = $_SESSION["senha"] ?? NULL;
?>
~~~

### Podemos agora montar um html simples para exibir os dados 

~~~php
<h1>Login: <?=$login?></h1>
<h1>Senha: <?=$senha?></h1>
~~~

### Por fim colocamos alguns estilos para ficar mais bonito e divertido gerando o código do começo do arquivo.
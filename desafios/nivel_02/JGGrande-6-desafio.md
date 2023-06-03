# Desafio 6 concluido com sucesso!

~~~php
<?php 
$pdo = new PDO("mysql:host=localhost;dbname=ex6;port=8889;charset=utf8;", "root", "root");

$sql = "SELECT nome FROM hello";
$dados = $pdo->prepare($sql);
$dados->execute();
$dados = $dados->fetch(PDO::FETCH_OBJ);
print_r("Hello ". $dados->nome);

~~~

## Primeiro fazemos a conecção com o banco de dados com o metodo 
~~~php
$pdo = new PDO("mysql:host=localhost;dbname=ex6;port=8889;charset=utf8;", "root", "root");
~~~
### PAssando as informações como o host que está o host, a porta, a identificação de acentuação, o nome, o usuario e a senha do banco de dados

~~~php
$sql = "SELECT nome FROM hello";
$dados = $pdo->prepare($sql);
$dados->execute();
$dados = $dados->fetch(PDO::FETCH_OBJ);
print_r("Hello ". $dados->nome);
~~~

### Faz um SELECT simples que mostra dados do banco
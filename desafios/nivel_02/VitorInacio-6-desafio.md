#### Atividade 6

~~~ php

<?php

$servidor = "localhost";
$usuario  = "root";
$senha    = "root";
$banco    = "ex6";

$pdo = new PDO("mysql:host={$servidor};dbname={$banco};port=8889;charset=utf8;",$usuario,$senha);
?>
~~~
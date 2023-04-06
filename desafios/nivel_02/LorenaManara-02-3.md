<?php
$senha = base64_encode("12345");
echo $senha;

$senha2 = base64_decode($senha);
echo $senha2;

?>